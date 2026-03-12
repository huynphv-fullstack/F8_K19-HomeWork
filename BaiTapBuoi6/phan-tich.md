Câu 1: Selector nào có độ ưu tiên cao nhất trong CSS?
    Selector có độ ưu tiên cao nhất là Inline CSS (style viết trực tiếp trong thẻ HTML).
    Thứ tự ưu tiên của CSS từ cao xuống thấp:
    1.Inline style (style="")
    2.ID selector (#id)
    3.Class selector (.class)
    4.Tag selector (h1, p, div...)
    Do đó khi nhiều selector cùng áp dụng cho một phần tử thì selector có độ ưu tiên cao hơn sẽ được áp dụng.

Câu 2: Nếu một phần tử HTML có cả h1, .title, và #main cùng set color — selector nào thắng? Tại sao?
    Selector #main (ID selector) sẽ thắng.
    Kết quả hiển thị sẽ là màu xanh lá (green) vì ID selector có độ ưu tiên cao hơn class và tag.

Câu 3: Nếu bạn thêm style="color: pink" trực tiếp vào phần tử ở Câu 2, kết quả thay đổi như thế nào?
    Kết quả hiển thị sẽ là màu hồng (pink).
    Lý do: Inline CSS có độ ưu tiên cao nhất, nên nó sẽ override tất cả các selector khác như id, class hoặc tag.

Câu 4: Tại sao theme.css có thể override style từ base.css? Điều kiện để override thành công là gì?
    theme.css có thể override base.css vì file CSS được load sau sẽ ghi đè file load trước nếu selector có cùng độ ưu tiên.
    Điều kiện để override thành công:
    1.theme.css phải được link sau base.css
    2.selector trong theme.css phải có độ ưu tiên bằng hoặc cao hơn selector trong base.css

Câu 5: Trong project của bạn, có hai phần tử đều dùng class .title nhưng hiển thị màu khác nhau. Giải thích tại sao.
    Hai phần tử dùng .title có thể hiển thị màu khác nhau vì:
    -Một phần tử có thêm ID selector
    -Hoặc có Inline CSS
    -Hoặc bị Internal CSS override
    -Hoặc bị theme.css override base.css

Câu 6: Phần tử nào trong project của bạn có CSS phức tạp nhất? Liệt kê các selector tác động lên nó và giải thích selector nào thắng cuối cùng.
    Phần tử có CSS phức tạp nhất là trong trang dashboard/index.html:
    <h1 class="title" id="special" style="color:red">DASHBOARD</h1>
    Các selector tác động lên phần tử này:
    -Tag selector: h1
    -Class selector: .title
    -ID selector: #special
    -External CSS: base.css
    -External CSS: theme.css
    -Internal CSS
    -Inline CSS: style="color:red"
    Selector thắng cuối cùng là Inline CSS vì nó có độ ưu tiên cao nhất trong CSS.
    Do đó màu hiển thị cuối cùng của tiêu đề là red