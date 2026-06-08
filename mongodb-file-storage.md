MongoDB stores files as Binary Data (BSON Binary).

For small files, you can store the binary data directly inside a document:

{
  "fileName": "photo.jpg",
  "fileData": <binary_data>
}
For large files: GridFS

MongoDB provides GridFS, which is designed for files larger than 16 MB (MongoDB's document size limit).

GridFS splits a file into smaller chunks and stores them in two collections:

fs.files → file metadata
fs.chunks → actual file chunks

Example:

video.mp4
    ↓
Split into chunks
    ↓
fs.files      (name, size, upload date)
fs.chunks     (chunk1, chunk2, chunk3...)

When you request the file, MongoDB reassembles the chunks.

In real-world applications

Many applications do not store large images/videos directly in MongoDB. Instead:

Upload file to cloud storage (e.g., AWS S3).
Store only the file URL/path in MongoDB.

Example:

{
  "name": "Profile Photo",
  "url": "https://storage.example.com/photo.jpg"
}

This is usually more scalable and cost-effective for large media files.

Interview Answer

Yes, MongoDB can store images, videos, PDFs, and other files. Small files can be stored as BSON binary data, while large files are typically stored using GridFS, which divides files into chunks and stores them across multiple documents. In production systems, large media files are often stored in external storage services, with only their URLs saved in MongoDB.
