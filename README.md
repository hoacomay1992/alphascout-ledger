# AlphaScout signal ledger

`hashes.log` has one line per trading session: `<date> <hash>`. The hash is the SHA-256 of that
session's ledger entry (every strategy's score report, written once after the close), serialized as
canonical JSON: sorted keys, separators `,` and `:`, UTF-8. Each entry also holds the hash of the
entry before it, so the entries form a chain. This repository's history shows when each hash was
published; an entry shown later can be checked against it, and nothing can be rewritten unnoticed.

Mỗi dòng của `hashes.log` là `<ngày> <hash>` của một phiên: hash SHA-256 của bản ghi sổ cái phiên
đó (báo cáo chấm điểm của mọi chiến lược, ghi một lần sau giờ đóng cửa). Lịch sử commit của repo
cho biết hash được công bố lúc nào; bản ghi đưa ra sau này đối chiếu được với hash đã công bố.
