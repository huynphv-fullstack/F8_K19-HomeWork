Câu 1: Selector nào có độ ưu tiên cao nhất trong CSS?
    Selector có độ ưu tiên cao nhất trong CSS thông thường là Inline CSS (style viết trực tiếp trong thẻ HTML).

Câu 2: Nếu một phần tử HTML có cả h1, .title, và #main cùng set color — selector nào thắng? Tại sao?
    Selector ID (#main) sẽ thắng.
    Lý do: ID selector có độ ưu tiên cao hơn class và tag selector trong CSS specificity.

Câu 3: Nếu bạn thêm style="color: pink" trực tiếp vào phần tử ở Câu 2, kết quả thay đổi như thế nào?
    Kết quả: màu hồng (pink).
    Lý do: Inline CSS có độ ưu tiên cao hơn ID selector, nên nó sẽ ghi đè tất cả các style khác.

Câu 4: Tại sao theme.css có thể override style từ base.css? Điều kiện để override thành công là gì?
    theme.css có thể override base.css khi:
    1. theme.css được load sau base.css trong HTML
    2. Selector trong theme.css có độ ưu tiên bằng hoặc cao hơn
    3. Hai CSS cùng áp dụng cho cùng một thuộc tính

Câu 5: Trong project của bạn, có hai phần tử đều dùng class .title nhưng hiển thị màu khác nhau. Giải thích tại sao.
    Điều này có thể xảy ra vì:
    - Một phần tử có thêm ID selector
    - Một phần tử có inline CSS
    - Một phần tử nằm trong selector cụ thể hơn (ví dụ .header .title)
    - Hoặc CSS được ghi đè bởi file CSS khác

Câu 6: Phần tử nào trong project của bạn có CSS phức tạp nhất? Liệt kê các selector tác động lên nó và giải thích selector nào thắng cuối cùng.
    Phần tử có CSS phức tạp nhất là trong trang dashboard/index.html:
    <h1 class="title" id="special" style="color:seafoam">DASHBOARD</h1>
    Các selector tác động lên phần tử này:
    - Tag selector: h1
    - Class selector: .title
    - ID selector: #special
    - External CSS: base.css
    - External CSS: theme.css
    - Internal CSS
    - Inline CSS: style="color:seafoam"
    Selector thắng cuối cùng là Inline CSS vì nó có độ ưu tiên cao nhất trong CSS.
    Do đó màu hiển thị cuối cùng của tiêu đề là seafoam.