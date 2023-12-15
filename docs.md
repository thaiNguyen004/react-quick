React Quickly
SECOND EDITION

brief contents
Chapter 1 - Meeting React
1.1	Benefits of using React
1.1.1 Simplicity
1.1.2 Speed and testability
1.1.3 Ecosystem and community
1.2 Disadvantages of React
1.3 How React can fit into your website
1.3.1 Single-page applications and React
1.3.2 The React stack
1.4 Your first React app: Hello World
1.4.1 The result
1.4.2 Writing the application
1.4.3 Installing and running a web server
Summary
Chapter 2 – Baby steps with React
2.1 Creating a new React app
2.1.1 React project commands
2.1.2 File structure
2.1.3 Templates
2.1.4 Pros and cons
2.2 A note about the examples in this book
2.3 Nesting elements
2.3.1 Node hierarchy
2.3.2 Simple nesting
2.3.3 Siblings
2.4 Creating custom components
2.5 Working with properties
2.5.1 A single property
2.5.2 Multiple properties
2.5.3 The special property: children
2.6 Application structure
2.7 Quiz
Summary
Chapter 3 - Introduction to JSX
3.1 Why do we use JSX?
3.1.1 Before and after JSX
3.1.2 Keeping HTML and JavaScript together
3.2 Understanding JSX
3.2.1 Creating elements with JSX
3.2.2 Using JSX with custom components
3.2.3 Multiline JSX objects
3.2.4 Outputting variables in JSX
3.2.6 Branching in JSX
3.2.7 Comments in JSX
3.2.8 Lists of JSX objects
3.2.9 Fragments in JSX
3.3 How to transpile JSX
3.4 React and JSX gotchas
3.4.1 Self-closing elements
3.4.2 Special characters
3.4.3 String conversion
3.4.4 The style attribute
3.4.5 Reserved names: class and for
3.4.6 Multiword attributes
3.4.7 Boolean attribute values
3.4.8 Whitespace
3.4.9 data- attributes
3.5 Quiz
Summary


Chapter 1 - Meeting React

This chapter covers
 Understanding what React is
 Solving problems with React
 Fitting React into your web applications
 Writing your first React web app: Hello World

React là công cụ đột phá mà các nhà phát triển web có thể chưa biết là cần thiết, nhưng không thể từ bỏ sau khi họ đã thử nghiệm. Điều này chắc chắn đúng đối với hai tác giả của cuốn sách này, cũng như nhiều nhà phát triển web nhiệt huyết khác trên khắp thế giới. React đang rất phổ biến—và với lý do đúng đắn.

Nếu bạn đã làm phát triển web vào đầu những năm 2000, tất cả những gì bạn cần chỉ là một số HTML và một ngôn ngữ phía máy chủ như Perl hoặc PHP. À, những ngày đẹp trời cũ của việc thêm các hộp alert() chỉ để gỡ lỗi mã nguồn frontend của bạn. Internet đã phát triển rất nhiều từ đó, và sự phức tạp của việc xây dựng trang web đã tăng đáng kể.

Trang web đã trở thành ứng dụng web với giao diện người dùng (UI) phức tạp, logic kinh doanh và các lớp dữ liệu đòi hỏi sự thay đổi và cập nhật theo thời gian—đôi khi là trực tiếp.

Nhiều JavaScript template libraries đã được viết để giải quyết vấn đề của UIs phức tạp. Nhưng chúng vẫn yêu cầu các nhà phát triển tuân thủ nguyên tắc phân tách cũ (Cascading Style Sheets [CSS], data and structure [HTML], và tương tác động dynamic interactions [JavaScript]) và chúng không đáp ứng đúng nhu cầu ngày nay (nhớ DHTML không?).

Ngược lại, React đưa ra một phương pháp mới, khi sử dụng đúng cách, giúp tối ưu hóa phát triển web frontend. React là một thư viện UI mạnh mẽ cung cấp một lựa chọn khác mà nhiều công ty lớn như Facebook, Netflix và Airbnb đã áp dụng và xem đó là hướng tiến. Thay vì defining một template duy nhất one-off template cho UI của bạn, React cho phép bạn tạo ra các thành phần UI UI components có thể tái sử dụng trong JavaScript mà bạn có thể sử dụng lại và lại trên trang web của mình.

Bạn cần một captcha control hoặc chọn ngày date picker? Sử dụng React để define một thành phần <Captcha/>hoặc <DatePicker/> component mà bạn có thể thêm vào form  của mình: một thành phần thả và thả đơn giản với tất cả chức năng và logic để giao tiếp với phía máy chủ. Bạn cần một hộp tự động hoàn tất autocomplete box mà truy vấn cơ sở dữ liệu không đồng bộ sau khi người dùng đã gõ bốn chữ trở lên? Define một thành phần <Autocomplete charNum="4"/> để thực hiện truy vấn không đồng bộ đó. Bạn có thể chọn liệu nó có giao diện hộp văn bản hay không, hoặc có thể sử dụng một phần tử biểu mẫu tùy chỉnh khác—có thể là <Autocomplete textbox="..." />.

Phương pháp approach này không mới. Việc tạo composable UIs đã tồn tại từ lâu, nhưng React là người đầu tiên sử dụng JavaScript thuần túy mà không cần template để làm cho điều này trở nên khả thi. Và phương pháp này đã chứng minh dễ dàng duy trì, sử dụng lại và mở rộng hơn.

React là một thư viện tuyệt vời để xây dựng UI, và nó nên là một phần của bộ công cụ phát triển web frontend của bạn, nhưng nó không phải là một giải pháp hoàn chỉnh cho tất cả các phát triển web frontend. Chúng ta sẽ dành một phần của chương này để xem xét ưu và nhược điểm của việc sử dụng React trong ứng dụng của bạn và cách React có thể phù hợp vào ngăn xếp phát triển web hiện tại của bạn.

Trong cuốn sách này, chúng tôi sẽ tập trung vào cơ bản của React và không đi sâu hơn, cung cấp cho độc giả một nền tảng vững chắc về các khái niệm và nguyên tắc cơ bản của thư viện React mà không đi vào các chủ đề ngoại vi hoặc nâng cao. Bằng việc tập trung chỉ vào React, độc giả sẽ có hiểu biết toàn diện về khả năng của nó và sẽ được trang bị đầy đủ để áp dụng kiến thức của mình vào một loạt các dự án phát triển web. LƯU Ý: Mã nguồn cho ví dụ trong chương này có sẵn tại https://rq2e.com/ch01.

1.1	Benefits of using React

Mỗi thư viện hoặc framework mới đều tuyên bố rằng nó tốt hơn các đối tác tiền nhiệm của mình ở một số mặt nào đó. Ban đầu, chúng ta có jQuery, và nó đã vượt bậc so với việc viết mã nguồn chung cho nhiều trình duyệt bằng JavaScript nguyên thuỷ. Nếu bạn nhớ JavaScript từ những ngày đầu, một single server request sẽ tốn rất nhiều dòng mã, vì phải tính đến Internet Explorer và các trình duyệt giống WebKit. Với jQuery, điều này chỉ mất một dòng duy nhất: $.ajax(), ví dụ. Ngày xưa, jQuery ở một số khía cạnh được biết đến như một framework—nhưng không còn nữa! Bây giờ một framework là một thứ gì đó lớn hơn và mạnh mẽ hơn.
Tương tự, với Backbone và sau đó là Angular, mỗi thế hệ mới của các framework JavaScript đã mang đến điều gì đó mới mẻ. React không độc đáo unique trong điều này. Điều mới là React thách thức một số khái niệm cơ bản được sử dụng bởi hầu hết các framework phổ biến trên frontend, ví dụ như ý tưởng rằng bạn cần phải có các templates.
Dưới đây là một số lợi ích của React so với các thư viện và framework khác tồn tại vào thời điểm React xuất hiện:
- Ứng dụng web đơn giản hơn Simpler web apps —React sử dụng kiến trúc dựa trên thành phần (Component-Based Architecture - CBA) với JavaScript thuần túy pure; một declarative style; mạnh mẽ, thân thiện với nhà phát triển Document Object Model (DOM) abstractions (không chỉ là DOM, mà còn iOS, Android, v.v.).
- Fast UIs —React cung cấp hiệu suất xuất sắc nhờ DOM ảo virtual DOM và smart reconciliation algorithm, điều này cũng mang lại lợi ích phụ là bạn có thể thực hiện kiểm thử mà không cần khởi động (bắt đầu) một trình duyệt không đồ họa.
- Ít mã để viết—Cộng đồng lớn và hệ sinh thái rộng lớn của các thành phần React cung cấp cho nhà phát triển nhiều thư viện và thành phần. Điều này quan trọng khi bạn đang xem xét framework nào để sử dụng cho phát triển.
Nhiều tính năng đã làm cho việc làm việc với React trở nên đơn giản hơn so với hầu hết các framework frontend khác có sẵn khi nó mới ra mắt. Tuy nhiên, nhiều framework mới đã xuất hiện kể từ khi React xuất hiện. Một phần là do sự phổ biến của React, một số framework mới này đã được phát triển với những lợi ích hoặc quan điểm tương tự, mỗi cái có một chút sửa đổi theo cách khác nhau. Một số framework khác có thể chỉ được truyền cảm hứng từ ý tưởng chung, nhưng lại hoạt động hoàn toàn khác nhau, trong khi một số khác rất giống với React, chỉ có một tập tính năng nhỏ hơn, đòi hỏi bạn đôi khi phải viết nhiều mã hơn, nhưng đổi lại có một mã nguồn ứng dụng nhỏ hơn nhiều.

Chúng ta sẽ xem xét những lợi ích làm cho React phổ biến. Đây là những điểm chính của React và chúng đã làm cho framework trở nên độc đáo khi ra mắt, mặc dù các framework hiện đại khác cũng có những lợi ích tương tự ngày nay. Hãy bắt đầu giải mã từng lợi ích một, bắt đầu với cách React thực sự dễ sử dụng.

1.1.1 Simplicity
Khái niệm về sự đơn giản trong khoa học máy tính được đánh giá cao bởi các nhà phát triển và người sử dụng, nhưng nó không tương đương với sự dễ sử dụng. Một điều đơn giản có thể khó triển khai, nhưng cuối cùng nó sẽ trở nên thanh lịch và hiệu quả hơn. Và thường, một điều dễ dàng cuối cùng sẽ trở nên phức tạp. Sự đơn giản chặt chẽ liên quan chặt chẽ đến nguyên tắc KISS (keep it simple, stupid - giữ nó đơn giản, ngốc nghếch). Ý chính là các hệ thống đơn giản hoạt động tốt hơn.
Phương pháp của React cho phép solutions đơn giản thông qua một trải nghiệm phát triển web đáng kể cải thiện cho các kỹ sư phần mềm. Khi chúng tôi bắt đầu làm việc với React, đó là một sự chuyển đổi đáng kể theo hướng tích cực, nhắc chúng tôi đến việc chuyển từ việc sử dụng JavaScript thuần túy không framework sang jQuery.
Trong React, sự đơn giản này được đạt được thông qua các tính năng sau:
- Phong cách Declarative hơn là Phong cách imperative—React chấp nhận phong cách mô tả hơn là mệnh lệnh bằng cách tự động cập nhật các hiển thị.
- CBA sử dụng JavaScript thuần túy—React không sử dụng domain-specific languages (DSLs) cho các thành phần của nó, chỉ sử dụng JavaScript thuần túy. Và không có sự phân tách khi làm việc trên cùng một chức năng.
- Powerful abstractions —React có một cách đơn giản để tương tác với DOM, cho phép bạn chuẩn hóa xử lý sự kiện và các giao diện khác hoạt động tương tự trên nhiều trình duyệt.
DECLARATIVE OVER IMPERATIVE STYLE
Phong cách Declarative có nghĩa là các nhà phát triển viết như nó nên làm how it should be, không phải là bước từng bước làm gì (imperative). Nhưng tại sao declarative style lại là sự lựa chọn tốt hơn? Lợi ích là declarative style giảm độ phức tạp và làm cho mã nguồn của bạn dễ đọc và hiểu hơn. Sự phân biệt giữa imperative style và declarative có thể trở nên học thuật đến một mức độ nào đó. Khi đưa ra cực đoan, lập trình declarative có thể trở nên rất phức tạp để đọc trừ khi bạn hiểu rõ một số khái niệm phức tạp như monads và functors. Dưới đây là một số cách khác nhau để mô tả sự khác biệt giữa hai phong cách này:
- Statements so với versus expressions—Lập trình theo Imperative-style thường làm việc với các câu lệnh statements độc lập mỗi cái tác động đến trạng thái chương trình, trong khi declarative programming sử dụng các biểu thức expressions xây dựng lên nhau để tiến triển luồng logic.
- Reserved word usage —Lập trình theo kiểu imperative thường sử dụng nhiều từ khóa dành riêng như for, while, switch, if, và else, trong khi lập trình declarative sử dụng các array methods, arrow functions, object access, Boolean expressions, và toán tử ba ngôi để đạt được cùng một kết quả.
- Function composition—Imperative-style programming thường sử dụng các cuộc gọi hàm độc lập và triệu hồi phương thức, trong khi declarative-style programming sử dụng function composition để xây dựng lên biểu thức trước đó và tạo ra các đoạn mã nhỏ tổng quát, khi hợp thành lại đạt được kết quả mong muốn.
- Khả năng biến đổi Mutability— Imperative-style programming thường sử dụng các đối tượng có thể biến đổi và thay đổi cấu trúc hiện tại, trong khi declarative-style programming sử dụng dữ liệu không thể biến đổi và tạo ra cấu trúc mới từ cấu trúc cũ thay vì chỉnh sửa cấu trúc hiện tại.
Hãy tạo một ví dụ đơn giản để minh họa những điểm khác nhau này. Mục tiêu của nhiệm vụ này là tạo ra một function, countGoodPasswords, mà khi được đưa vào một danh sách mật khẩu, sẽ trả về số lượng mật khẩu tốt. Ở đây, chúng ta sẽ định nghĩa một mật khẩu tốt là bất kỳ mật khẩu nào dài ít nhất chín ký tự. Đây là một nhiệm vụ đơn giản tuyệt vời có thể giải quyết bằng bất kỳ ngôn ngữ lập trình nào theo nhiều cách khác nhau. Một số ngôn ngữ lập trình tự nhiên khiến cho một kiểu lập trình trở nên tự nhiên hơn, nhưng JavaScript đặc biệt, vì nó là thành viên của cả hai thế giới. Bạn có thể giải quyết nhiệm vụ này theo kiểu imperative hoặc declarative.

Let’s start with a (very) naive imperative solution:
function countGoodPasswords(passwords) {
    const goodPasswords = []; [1] 
    for (let i = 0; i < passwords.length; i++) { [2]
        const password = passwords[i]; [1]
        if(password.length < 9) {		[2]
            continue;
        }
        goodPasswords.push(password); [1]
    }
    return goodPasswords.length;
}

1.	Câu lệnh mới thay đổi trạng thái của chương trình.
2.	Từ khóa dành riêng kiểm soát luồng của chương trình.


Hãy triển khai ví dụ này sử dụng tư duy mindset declarative programming:

function countGoodPasswords(passwords) {
    return passwords.filter(p => p.length >= 9).length;
}

Chúng ta đến trực tiếp mục tiêu chỉ trong một câu lệnh bằng cách điều khiển một đối tượng trong nhiều bước, sử dụng function composition để đạt được mục tiêu. Chúng ta lọc mảng gốc để đạt được một giá trị tạm thời, đó là mảng chỉ chứa mật khẩu tốt. Tuy nhiên, chúng ta không bao giờ lưu trữ mảng này ở bất kỳ đâu; chúng ta chuyển trực tiếp sang bước tiếp theo là lấy độ dài của mảng đó.
Đó chỉ là một số mã nguồn JavaScript chung chung. Làm thế nào điều này liên quan đến React? React sử dụng cùng một declarative solution khi bạn xây dựng các giao diện người dùng (UIs). Đầu tiên, React developers describe các UI elements theo declarative style. Sau đó, khi có sự thay đổi đối với các hiển thị được tạo ra bởi những phần tử UI đó, React chịu trách nhiệm về các cập nhật. Hoan hô!
Sự thuận tiện của React’s declarative style đặc biệt nổi bật khi bạn cần thay đổi hiển thị make
changes to the view. Đó được gọi là những thay đổi của trạng thái nội tại internal state.. Khi trạng thái thay đổi, React cập nhật hiển thị một cách tương ứng.

LƯU Ý: Chúng ta sẽ tìm hiểu cách states hoạt động trong chương 5.

COMPONENT-BASED ARCHITECTURE USING PURE JAVASCRIPT
CBA (Component-Based Architecture) tồn tại trước khi React xuất hiện trên trường. Phân tách vấn đề, kết nối lỏng lẻo và tái sử dụng mã nguồn là cốt lõi của phương pháp này vì nó mang lại nhiều lợi ích; kỹ sư phần mềm, bao gồm cả những nhà phát triển web, yêu thích CBA. Một building block của CBA trong React là lớp thành phần (component class). Như với các CBA khác, nó mang lại nhiều lợi ích, với việc tái sử dụng mã nguồn là chủ yếu (bạn có thể viết ít mã nguồn hơn!).
Trước khi có React, điều thiếu sót là một triển khai JavaScript thuần túy của kiến trúc này. Khi bạn làm việc với Angular, Backbone, Ember hoặc hầu hết các framework frontend khác giống Model-View-Controller (MVC), bạn có một tệp JavaScript và một tệp template khác nhau. (Angular sử dụng thuật ngữ directives cho các thành phần.) 
Có một số vấn đề khi có hai ngôn ngữ (và hai hoặc nhiều files) cho một component duy nhất. Phân tách HTML và JavaScript hoạt động tốt khi bạn phải tạo HTML trên máy chủ, và JavaScript chỉ được sử dụng để làm cho văn bản của bạn nhấp nháy. Bây giờ, ứng dụng trang đơn (SPAs) xử lý đầu vào phức tạp từ người dùng và thực hiện quá trình hiển thị trên trình duyệt. Điều này có nghĩa là HTML và JavaScript được kết nối chặt chẽ chức năng. Đối với nhà phát triển, không cần phải tách rời HTML và JavaScript khi làm việc trên một phần của dự án (component).

Bên trong, React sử dụng một DOM ảo để tìm sự khác biệt (delta) giữa những gì đã có trong trình duyệt và hiển thị mới. Quá trình này được gọi là DOM diffing hoặc reconciliation of state and view (mang chúng trở lại sự tương tự). Điều này có nghĩa là nhà phát triển không cần phải lo lắng về việc thay đổi hiển thị một cách rõ ràng; tất cả những gì họ cần làm là cập nhật trạng thái và hiển thị sẽ được cập nhật tự động khi cần. Bạn sẽ thấy chúng tôi sử dụng nguyên tắc này một cách ngầm định lần lượt trong cuốn sách. Chúng tôi không bao giờ thao tác DOM trực tiếp; chúng tôi để React thực hiện công việc đó thay cho chúng tôi.
Ngược lại, với jQuery, bạn sẽ cần thực hiện các cập nhật một cách mệnh lệnh. Bằng cách thao tác DOM, nhà phát triển có thể thay đổi một số phần của trang web mà không cần vẽ lại toàn bộ trang. Thao tác DOM là điều bạn thực hiện khi gọi các phương thức jQuery.
Hãy tưởng tượng sự hỗ trợ được cung cấp bởi framework cơ bản trên một thang đo như được hiển thị trong hình 1.1. Ở một đầu của thang đo, bạn có một "framework" thực sự không giúp bạn một chút nào. Nếu bạn xây dựng ứng dụng của mình bằng JavaScript thuần túy, bạn sẽ ở ở cực điểm này. Sử dụng jQuery sẽ làm cho việc thao tác DOM trở nên dễ dàng hơn, nhưng bạn vẫn không có sự giúp đỡ nào từ framework khi có sự cập nhật. Bạn sẽ phải đảm bảo thủ công rằng các hiển thị jQuery của bạn cập nhật khi dữ liệu jQuery của bạn cập nhật.
 

Ở đầu còn lại của thang đo, chúng ta có các framework như Angular, một framework khác rất phổ biến và có thể so sánh với React mọi cách. Tuy nhiên, Angular hoạt động theo cách cơ bản khác với nhiều "ma thuật" diễn ra ẩn sau màn hình. Bạn thường chỉ mô tả cách các thành phần của bạn tương tác, và Angular sẽ cố gắng kết nối mọi thứ một cách đúng đắn ẩn sau màn hình. Vấn đề với Angular là bạn thường mất sự kiểm soát tinh tế mong muốn nếu mọi thứ không hoạt động đúng cách. Nhiều điều được che giấu khỏi bạn, điều này làm cho mọi thứ trở nên không cần thiết phức tạp.

React đạt được điều đó ở mức trung bình, nơi framework giúp bạn với nhiều công việc nhàm chán của việc kết nối các thành phần khác nhau ẩn sau màn hình, nhưng không khóa chặt bạn khỏi sự kiểm soát tinh tế cần thiết để tạo ra ứng dụng web phức tạp. Điều này rõ ràng là một ý kiến chủ quan, nhưng chúng tôi không đơn độc trong cách cảm nhận này.

POWERFUL ABSTRACTIONS
React được trang bị các trừu tượng tuyệt vời great abstractions sau đây, giúp cuộc sống của nhà phát triển React trở nên dễ dàng hơn:
- Sự kiện tổng hợp Synthetic events trừu tượng hóa sự khác biệt của trình duyệt trong các native events
- JavaScript XML (JSX) trừu tượng hóa JS DOM
- Độc lập với trình duyệt Browser independence cho phép hiển thị trong môi trường không phải trình duyệt nonbrowser (ví dụ, trên máy chủ)

React có một powerful abstraction của browser event model. Nó ẩn đi các giao diện cơ bản và cung cấp các phương thức và thuộc tính được chuẩn hóa/tổng hợp normalized/synthesized. Ví dụ, khi bạn tạo một sự kiện onClick trong React, thay vì trình xử lý sự kiện nhận một native browser–specific event object, nó nhận một synthetic event object là một lớp bọc quanh các event object cụ thể cho trình duyệt. Bạn có thể mong đợi cùng một hành vi từ các synthetic events bất kể trình duyệt bạn chạy mã. React cũng có một set of synthetic events cho sự kiện chạm, thích hợp để xây dựng ứng dụng web cho các thiết bị di động.

Tiếp theo là JSX, đây là một trong những phần gây tranh cãi về React. Đối với một số người, sự trừu tượng hóa của JSX là một lý do mạnh mẽ để sử dụng React, trong khi JSX đã là một chướng ngại hoặc thậm chí là một yếu tố cản trở đối với người khác. Nếu bạn đã quen với Angular, thì bạn đã phải viết rất nhiều mã JavaScript trong mã mẫu của mình vì trong phát triển web hiện đại, HTML thuần túy quá tĩnh lặng và ít có ích. Lời khuyên của chúng tôi là hãy đánh giá cao React và đưa JSX một cơ hội công bằng.
JSX là một cú pháp phức tạp hơn JavaScript để viết các React elements trong JavaScript bằng cách sử dụng cú pháp giống như HTML với <>. React kết hợp tốt với JSX vì nhà phát triển có thể triển khai và đọc mã nguồn tốt hơn. Hãy xem JSX như một ngôn ngữ con được biên dịch thành JavaScript nguyên bản. Vì vậy, JSX không chạy trên trình duyệt mà được sử dụng làm mã nguồn để biên dịch. Dưới đây là một đoạn mã ngắn viết bằng JSX:
if(user.session) {
    return <a href="/logout">Logout</a>;
} else {
    return <a href="/login">Login</a>;
}

Ngay cả khi bạn tải một tệp JSX trong trình duyệt của bạn với thư viện biến đổi thời gian chạy biên dịch JSX thành JavaScript nguyên bản, bạn vẫn không chạy JSX; bạn chạy JavaScript thay vào đó. Ở trong điều này, JSX tương tự như CoffeeScript. Bạn biên dịch những ngôn ngữ này thành JavaScript nguyên bản để có cú pháp và tính năng tốt hơn so với JavaScript thông thường.
Chúng tôi biết rằng đối với một số người, việc có HTML xen kẽ giữa mã nguồn JavaScript trông lạ lẫm. Mất một khoảng thời gian đối với mỗi nhà phát triển React mới (bao gồm cả chúng tôi) để thích ứng vì chúng tôi đang mong đợi một syntax error messages. Và đúng, việc sử dụng JSX là tùy chọn. Vì hai lý do này, chúng tôi sẽ không đề cập đến JSX cho đến chương 3. Tin tưởng chúng tôi, nó rất mạnh mẽ và thậm chí là gây nghiện khi bạn quen thuộc với nó.

Một ví dụ khác về React’s DOM abstraction là bạn có thể hiển thị các React elements trên server. Điều này có thể hữu ích để search engine optimization (SEO) và cải thiện hiệu suất.
Có nhiều lựa chọn khi đến việc rendering React components trong cả DOM và HTML strings trên máy chủ. Bạn thậm chí có thể sử dụng các phương pháp hybrid nơi các template của bạn được hiển thị với một số nội dung trên máy chủ và sau đó được tái tạo với dữ liệu thực trong trình duyệt. Chúng tôi sẽ nói thêm nhiều về điều này trong phần 1.3. Và, nói về DOM, một trong những lợi ích mà mọi người tìm kiếm nhiều nhất ở React là hiệu suất tuyệt vời của nó.

1.1.2 Speed and testability
Ngoài các cập nhật DOM cần thiết, framework của bạn có thể thực hiện các cập nhật không cần thiết, làm cho hiệu suất của giao diện người dùng phức tạp trở nên tồi tệ hơn. Điều này trở nên đặc biệt rõ ràng và đau đớn cho người dùng khi bạn có nhiều phần tử giao diện người dùng động trên trang web của mình.
Ngược lại, React’s virtual DOM tồn tại chỉ trong JavaScript memory. Mỗi khi có sự thay đổi dữ liệu, React trước tiên so sánh sự khác biệt bằng cách sử dụng virtual DOM của mình; chỉ khi thư viện biết rằng có một thay đổi trong quá trình kết xuất, nó mới cập nhật DOM thực tế. Hình 1.2 mô tả tổng quan cấp cao về cách virtual DOM của React hoạt động khi có sự thay đổi dữ liệu.

 

Cuối cùng, React chỉ cập nhật những phần cần thiết để trạng internal state (virtual DOM) và view (real DOM) trở nên giống nhau. Ví dụ, nếu có một phần tử <p>, và bạn mở rộng văn bản thông qua trạng thái của thành phần, chỉ văn bản sẽ được cập nhật (tức là innerHTML), không phải phần tử chính nó. Điều này dẫn đến hiệu suất tăng lên so với việc kết xuất lại toàn bộ bộ phận các phần tử hoặc, thậm chí, toàn bộ trang (kết xuất phía máy chủ).
Các chi tiết táo bạo của reconciliation
Nếu bạn thích nghiên cứu về thuật toán và ký hiệu Big O, hai bài viết sau làm rất tốt công việc giải thích cách nhóm phát triển React đã biến một vấn đề  O(n3) thành một vấn đề O(n):

- "Reconciliation," trên trang web của React http://mng.bz/PQ9X
- "React’s Diff Algorithm" của Christopher Chedeau http://mng.bz/68L4

Lợi ích bổ sung của virtual DOM là bạn có thể thực hiện unit testing mà không cần trình duyệt không đầu (headless browsers) như PhantomJS ([http://phantomjs.org](http://phantomjs.org)). Có nhiều thư viện khác nhau, bao gồm Jest và React Testing Library, giúp bạn kiểm thử các thành phần của mình trực tiếp từ dòng lệnh. Chúng tôi sẽ giải thích chi tiết hơn về kiểm thử đơn vị của các thành phần và hook React trong các chương sau.
1.1.3 Ecosystem and community
Cuối cùng nhưng không kém phần quan trọng, React được hỗ trợ bởi các nhà phát triển của ứng dụng web quy mô lớn gọi là Facebook, cũng như là đồng đội của họ tại Instagram. Như với Angular và một số thư viện khác, sự hỗ trợ từ một công ty lớn mang lại một môi trường thử nghiệm đáng tin cậy (được triển khai trên hàng triệu trình duyệt), sự an tâm về tương lai và tăng tốc độ đóng góp. Điều này, tất nhiên, cũng là một rủi ro vì nếu Facebook đột ngột muốn đưa React theo một hướng mới, bạn có thể bị bỏ lại nếu bạn không thích hướng đó, vì vậy hãy cân nhắc kỹ lưỡng về lựa chọn của bạn.
Đã có nhiều nội dung tuyệt vời đã được cộng đồng tạo ra cho React. Bạn sẽ thấy rằng khi bạn cần một loại component hoặc giao diện nào đó, bạn có thể tìm kiếm trên web với từ khóa "react [tên của component]", và hơn 95% thời gian, bạn sẽ tìm thấy một cái gì đó đáng giá.

Lịch sử của phần mềm mã nguồn mở rõ ràng cho thấy rằng việc quảng bá các dự án mã nguồn mở cũng quan trọng như mã nguồn chính nó để được sự chấp nhận rộng rãi và thành công. Bằng việc nói đó, chúng tôi có ý là nếu một dự án có một trang web kém chất lượng, thiếu tài liệu và ví dụ, hoặc có một logo xấu xí, hầu hết các nhà phát triển sẽ không nghiêm túc với nó đặc biệt là hiện nay, khi có rất nhiều thư viện JavaScript. Nhà phát triển rất kén chọn và họ sẽ không sử dụng một thư viện xấu xí.
Như câu ngạn ngữ nói, "Đừng đánh giá một quyển sách qua bìa." Điều này có vẻ gây tranh cãi, nhưng, đáng tiếc, hầu hết mọi người, bao gồm cả kỹ sư phần mềm, thường có xu hướng có định kiến như là do branding tốt. May mắn thay, React có một danh tiếng kỹ thuật tốt ở phía sau nó. Và nói về bìa sách, chúng tôi hy vọng bạn không mua cuốn sách này chỉ vì bìa nó!

1.2 Disadvantages of React
Tất nhiên, hầu hết mọi thứ đều có nhược điểm của nó. Điều này cũng đúng với React, nhưng danh sách đầy đủ về các nhược điểm phụ thuộc vào người bạn hỏi. Một số khác biệt, như khía cạnh declarative so với imperative, là rất chủ quan. Chúng có thể là lợi ích hoặc nhược điểm tùy thuộc vào sở thích cá nhân của bạn. Dưới đây là danh sách nhược điểm của React (như bất kỳ danh sách nào, nó có thể thiên vị):

- React isn’t a full-blown, Swiss Army knife–type of framework  React không phải là một framework loại Swiss Army knife toàn diện. Nhà phát triển cần kết hợp nó với một thư viện như Redux hoặc XState để đạt được chức năng tương đương với Angular hoặc Ember. Điều này cũng có thể là một ưu điểm nếu bạn cần một thư viện UI tối giản để tích hợp vào ngăn xếp hiện tại của bạn.
- React stacks require maintenance and continuous package management  Ngăn xếp React đòi hỏi bảo trì và quản lý gói liên tục. Vì bạn không bao giờ chỉ sử dụng React một mình, mà hầu hết luôn kết hợp nó với một số package khác, bạn cần maintain liên tục các dependencies của mình và đảm bảo bạn đang sử dụng các phiên bản đúng của các gói khác nhau. Trong các dự án lớn, điều này có thể trở thành một nguồn công việc không cần thiết đáng kể.
- React uses a somewhat new approach to web development, and JSX and functional programming
can be intimidating to beginners.  React sử dụng một phương pháp mới đối với phát triển web, và JSX và lập trình hàm có thể làm kinh hãi đối với người mới học. Đặc biệt là trong những ngày đầu, có sự thiếu hụt về các phương pháp tốt nhất, sách hay, khóa học và tài nguyên có sẵn để nắm vững React và các framework tương tự. Chúng tôi sẽ thảo luận về JSX chi tiết hơn trong chương 3.

- React only has a one-way binding. React chỉ có một liên kết một chiều. Mặc dù liên kết một chiều là lợi ích hơn cho các ứng dụng web phức tạp và loại bỏ nhiều sự phức tạp, một số nhà phát triển (đặc biệt là những người phát triển Angular) đã quen với việc sử dụng liên kết hai chiều sẽ phải viết thêm một chút mã. Chúng tôi sẽ giải thích cách liên kết một chiều của React hoạt động so với liên kết hai chiều của Angular trong chương 9, nơi chúng ta sẽ đề cập đến làm việc với form data.
- React isn’t reactive (as in reactive programming and architecture, which are more eventdriven,
resilient, and responsive) out of the box  React không phải là reactive (như trong lập trình và kiến trúc reactive, nơi sự kiện, sự chịu đựng và tính phản ứng cao hơn) ngay từ đầu. Nhà phát triển cần sử dụng các thư viện khác, như thư viện React Query, để làm cho ứng dụng của họ tương thích với nội dung bên ngoài external content một cách mượt mà và phản ứng. Điều này cũng đòi hỏi nhà phát triển phải sử dụng một tư duy khác khi phát triển ứng dụng React, hoặc sẽ dẫn đến ứng dụng viết mã kém chất lượng khi cố gắng đưa React hình tròn round React vào một kiến trúc vuông square architecture. 

Để tiếp tục với giới thiệu về React, hãy xem cách nó tích hợp vào một ứng dụng web.

1.3 How React can fit into your website
Các trang web có nhiều biến thể variants, và React có thể được sử dụng để tạo nội dung tương tác interactive content trên nhiều loại trang web khác nhau, cả làm thay thế cho các công nghệ khác hoặc như một cách để thêm chức năng mới cho trang web của bạn. React có thể được sử dụng trên cả trang web "cổ điển" chủ yếu được rendered by a server cũng như client-side web applications, còn được biết đến là ứng dụng trang đơn single-page applications (SPA), như đã đề cập trước đó.
React core library chủ yếu là một thư viện UI. Thư viện core này có thể so sánh được với các thư viện UI khác, nhưng không trực tiếp so sánh được với các framework ứng dụng web toàn diện hơn như Angular. Tuy nhiên, kết hợp với các thư viện khác, cả do đội ngũ React phát triển hoặc các bên khác (ví dụ: React Router và Redux), React có thể là một đối thủ đầy đủ cho bất kỳ framework ứng dụng web nào.
Nếu bạn đang sử dụng một framework SPA khác (ví dụ: Angular, Vue, Ember, Backbone, vv.) để hiển thị ứng dụng web của bạn hiện tại, bạn có thể cần thay thế toàn bộ nó bằng một ngăn xếp dựa trên React. Việc tạo ra một SPA kết hợp một số phần được hiển thị bằng Angular, ví dụ, và các phần khác bằng React là rất khó và gần như không thể.
Bạn có thể sử dụng React chỉ cho một phần của UI nếu bạn có một trang web với các phần tương tác nhỏ (hoặc widget). Trong trường hợp như vậy, bạn có thể thay thế từng widget hiện tại của mình bằng các ứng dụng React nhỏ một cách từ từ mà không cần thay đổi mọi thứ khác. Những widget hiện tại này có thể được viết bằng plain JavaScript, jQuery, hoặc thậm chí là Angular hoặc các framework tương tự.

Khi bạn chuyển đổi từng widget sang React, bạn có thể đánh giá xem nó phù hợp tốt nhất với tổ chức của bạn.

React không phụ thuộc vào backend cho phát triển frontend. Nói cách khác, bạn không cần phải phụ thuộc vào backend dựa trên JavaScript (Node hoặc Deno) để sử dụng React. Việc sử dụng React với bất kỳ công nghệ backend nào khác, chẳng hạn như Java, Ruby, Go, hoặc Python, đều hoàn toàn khả thi. React là một thư viện UI, cuối cùng cùng thể tích hợp với bất kỳ backend và bất kỳ thư viện dữ liệu frontend nào (Backbone, Angular, Meteor, vv.).

Một trường hợp sử dụng phổ biến khác cho React là cho các trình tạo trang tĩnh static site generators. Trong cấu hình như vậy, React được sử dụng để define website của bạn cục bộ trong môi trường của bạn, nhưng khi deployed lên máy chủ thực, nó được render xuống " down " thành một trang web HTML thuần chỉ có JavaScript thực hiện một ít công việc để thêm tính tương tác. Tất cả các templates của bạn và các thứ khác sẽ đã được giải quyết. Ban đầu, điều này chủ yếu phổ biến cho các trang web nhỏ, chẳng hạn như các blog, mà không cập nhật quá thường xuyên.
Các tiến bộ gần đây trong server-side React rendering đã khiến phương pháp này được sử dụng ngày càng phổ biến hơn, ngay cả đối với các SPA lớn cập nhật thường xuyên. Bạn có thể làm điều này với các framework phổ biến được xây dựng trên React, chẳng hạn như Next.js hoặc Remix. Đây được coi là partially server-rendered web applications, trong đó mã React của bạn chạy cả trên máy chủ và ở phía máy khách. Bạn có thể, ví dụ, pre-render một danh sách trên server và thêm tùy chọn lọc và sắp xếp tương tác ở phía client. Điều này có thể nghe có vẻ một chút đáng sợ, nhưng các framework mới như Next.js và Remix làm cho nó tương đối dễ dàng.
Tóm lại cách React tích hợp vào một trang web, thường được sử dụng trong các tình huống sau:
- Là một thư viện UI trong một SPA, chẳng hạn như React+React Router+Redux.
- Là một widget có thể thay thế trong bất kỳ ngăn xếp frontend nào, chẳng hạn như một thành phần nhập React autocomplete trong một trang web được xây dựng bằng bất kỳ kết hợp công nghệ nào khác nhau.
- Là một trang web tĩnh được hiển thị khi triển khai để phục vụ nội dung ít được cập nhật thường xuyên.
- Là một trang web hoặc SPA có một phần được hiển thị phía máy chủ hoặc phần lớn là một framework mạnh mẽ hơn có thể được cung cấp nội dung từ một CMS bên ngoài, chẳng hạn như WordPress hoặc Contentful.
- Là một thư viện UI trong ứng dụng di động sử dụng React Native hoặc ứng dụng desktop sử dụng Electron.

React hoạt động tốt với một số công nghệ frontend, nhưng chủ yếu được sử dụng như một phần của các SPA. Chúng tôi sẽ giải thích cách React tích hợp vào một SPA trong phần tiếp theo.

1.3.1 Single-page applications and React

SPA (Single Page Applications) là một phần nhỏ của trang web nói chung. Một trang web được coi là SPA nếu nó có rất nhiều chức năng trực tiếp functionality directly có sẵn trong trình duyệt và không chỉ là thông tin. Ví dụ bao gồm Facebook, Google Docs, Gmail, và nhiều ứng dụng khác.
SPAs được xây dựng bằng cách sử dụng nhiều công nghệ, trong đó React chỉ là một phần tiềm ẩn trong ngăn xếp. Bạn thậm chí không thể sử dụng React một mình; ít nhất cần một vài công nghệ khác để React có thể sử dụng như một ứng dụng độc lập. Trong phần này, chúng ta sẽ xác định cái gì là SPA nói chung và sau đó chỉ ra cách React tích hợp vào cấu trúc này.

SPAs còn được biết đến là thick clients vì trình duyệt, là một client, chứa nhiều logic và thực hiện các chức năng như rendering HTML, validation, UI changes, và nhiều chức năng khác. Ngược lại với "thin clients," nơi client trình duyệt chỉ được sử dụng để hiển thị thông tin đã được máy chủ tạo ra trước. Trong mô hình thin client, trình duyệt thực hiện rất ít công việc.
Hình ảnh 1.3 là một high-level example về một SPA chung không phụ thuộc vào công nghệ sử dụng. Nó hiển thị một cái nhìn toàn cảnh về kiến trúc điển hình với a user, a browser, and a server. Hình ảnh mô tả một người dùng đưa ra yêu cầu và các hành động đầu vào như nhấp vào một nút, kéo và thả, di chuột, và những hành động khác.

 

Hãy đi qua quy trình điển hình từ đầu đến cuối này, theo các bước đánh số trong hình 1.3:

1. Người dùng gõ một URL vào trình duyệt để mở một trang mới.
2. Trình duyệt gửi URL request đến server.
3. Server phản hồi với các tài nguyên tĩnh static assets như HTML, CSS và JavaScript. Trong hầu hết các trường hợp, HTML chỉ là nền bare-bones; nghĩa là, nó chỉ có một kết cấu cơ bản của trang web skeleton. Thường có một thông báo " Loading . . . " và/hoặc hình quay vòng GIF.
4. Các tài nguyên tĩnh bao gồm mã JavaScript của ứng dụng. Khi được tải, mã này thực hiện các yêu cầu bổ sung để lấy dữ liệu.
5. Dữ liệu trả về dưới dạng JSON, XML hoặc bất kỳ định dạng nào khác.
6. Khi ứng dụng nhận được dữ liệu, nó có thể render HTML còn thiếu (khối User Interface trong hình). Nói một cách khác, quá trình UI rendering xảy ra trong trình duyệt khi ứng dụng đưa dữ liệu vào các templates đã được tạo trước, còn được biết đến là hydration. 
7. Khi quá trình render của trình duyệt hoàn thành, trình duyệt cập nhật nội dung được hiển thị, và người dùng có thể làm việc với ứng dụng.
8. Người dùng nhìn thấy một trang web đẹp. Người dùng có thể tương tác với trang (Đầu vào trong hình), kích thích các yêu cầu mới từ ứng dụng đến máy chủ, và chu kỳ các bước 2–6 tiếp tục. Tại giai đoạn này, có thể xảy ra browser routing nếu ứng dụng triển khai nó, có nghĩa là navigation đến một URL mới sẽ không kích hoạt việc tải lại trang mới từ máy chủ, mà thay vào đó là việc vẽ lại ứng dụng trong trình duyệt.

Tóm lại, trong một SPA, hầu hết quá trình vẽ cho UI diễn ra trong trình duyệt. Chỉ có dữ liệu di chuyển đến và từ trình duyệt. So sánh điều này với một trang web "classic", không phải là một SPA, nơi tất cả quá trình vẽ diễn ra trên máy chủ. React tích hợp vào kiến trúc SPA này trong các bước 6 và 8 bằng cách rendering nội dung dựa trên dữ liệu cũng như xử lý đầu vào của người dùng và cập nhật nội dung dựa trên dữ liệu cập nhật kết quả từ các đầu vào này.

1.3.2 The React stack
React không phải là một frontend JavaScript SPA framework toàn diện. React có tính nhẹ nhàng trong ý nghĩa là nó chỉ thực hiện một công việc (rendering reactive UIs) và cố gắng thực hiện công việc đó rất tốt. Nó không áp đặt một cách cụ thể để thực hiện các công việc như data modeling, styling hoặc routing (nó không có quan điểm cụ thể). Do đó, developers thường cần kết hợp React với một routing and/or data library.
Mặc dù bạn có thể sử dụng React như một phần nhỏ của ngăn xếp của bạn, nhưng developers thường chọn sử dụng một ngăn xếp tập trung vào React, bao gồm cả React core chính nó cũng như các thư viện dữ liệu, định tuyến và styling được tạo ra đặc biệt để sử dụng với React, như các thư viện sau:
- Data model libraries and backends - Examples include TanStack Query (https://
tanstack.com/query/latest), Redux (http://redux.js.org), Recoil.js (https://
recoiljs.org/), XState (https://xstate.js.org/), and Apollo (www.apollographql
.com/).
- Routing library - Thường là React Router (https://github.com/remix-run/react-router) hoặc một định tuyến tương tự được triển khai trong nhiều frameworks khác.
- Styling libraries - Hoặc một tập hợp được định nghĩa trước của các compoennt được thiết kế như Material UI (https://mui.com/) hoặc Bootstrap (https://react-bootstrap.github.io/), hoặc một thư viện để dễ dàng làm việc với CSS bên trong các thành phần React, như Styled-Components (https://styled-components.com/), Vanilla Extract (https://vanilla-extract.style/) hoặc thậm chí Tailwind CSS (https://tailwindcss.com/).
Hệ sinh thái của các thư viện cho React đang phát triển mỗi ngày. Ngoài ra, khả năng của React trong việc mô tả các composable components (các thành phần độc lập của UI self-contained chunks of the UI) làm cho việc tái sử dụng mã trở nên dễ dàng. Nhiều thành phần được đóng gói dưới dạng các module npm.
Một danh sách (được chọn lọc) tuyệt vời về nhiều React components khác nhau cho nhiều mục đích có thể được tìm thấy tại đây: https://github.com/brillout/awesome-react-components. Danh sách này có tất cả từ các components UI(bao gồm cả hàng loạt các form elements) đến các frameworks UI hoàn chỉnh, các tiện ích phát triển và công cụ kiểm thử.

React website frameworks
Một danh mục khác của các React frameworks là server-side framework toàn diện, lo chăm sóc mọi thứ cho bạn. Các framework như vậy có hai biến thể, nhưng đôi khi một framework có thể hoạt động theo cả hai cách:
 Static site generators (SSGs)
 Dynamic server-rendered React (SSR)
SSGs là những framework giúp tạo ra một trang web hoàn toàn tĩnh mà bạn có thể triển khai ngay lên bất kỳ static website host nào mà không đòi hỏi nhiều công việc từ bạn và không cần hosting đắt đỏ. Điều này đặc biệt phổ biến đối với các trang web cá nhân nhỏ như blog, nhưng cũng có thể được sử dụng cho các doanh nghiệp nhỏ và thậm chí các trang web thương mại điện tử nhỏ (không cần cập nhật quá thường xuyên).
Các framework SSR phức tạp hơn và sẽ quan tâm tới việc pre-rendering ứng dụng React của bạn trên server trước khi quan tâm tới HTML qua wire cho trình duyệt của khách truy cập. Điều này có nghĩa là chúng rất tốt cho SEO, ủng hộ khả năng chia sẻ và mang lại nhiều lợi ích khác. Dưới đây là ba framework SSR phổ biến:
- Gatsby Framework viết blog rất phổ biến này cũng hữu ích cho nhiều loại trang web tĩnh khác.

- Next.js Là một trong những React website framework phổ biến nhất, hữu ích cho cả các static websites nhỏ và những dự án lớn dynamic.

- Remix Đứa trẻ mới khá mới mẻ này đang nhanh chóng thu hút sự chú ý và phổ biến khi phục vụ super-fast dynamic React websites.
Tất cả các framework này - và nhiều hơn nữa - là các sự mở rộng khác nhau của React, mỗi cái hoạt động theo các mô hình riêng của nó. Chúng tất cả thêm các chức năng bổ sung trên nền React và đôi khi còn đi kèm với một bộ các thành phần React giúp bạn tạo ra trang web của mình để tận dụng đầy đủ các tính năng của framework.

Đến thời điểm này, bạn nên đã hiểu được React là gì, cấu trúc của nó, vị trí của nó trong ứng dụng web cấp cao, và cách bạn có thể sử dụng các công cụ được xây dựng dựa trên React để tạo ra các trang web phức tạp. Bây giờ là lúc bắt tay vào viết ứng dụng React đầu tiên của bạn.

1.4 Your first React app: Hello World

Hãy khám phá ứng dụng React đầu tiên của bạn bằng cách triển khai một ứng dụng Hello World - ví dụ quan trọng được sử dụng để học các ngôn ngữ lập trình (xem hình 1.4). Nếu chúng ta không làm điều này, thì thần thánh của lập trình có thể trừng phạt chúng ta.
 
Trước khi bắt đầu, bạn sẽ cần một số điều. May mắn thay, vì chúng ta đang phát triển một ứng dụng chạy trong trình duyệt, bạn không cần các trình biên dịch hoặc thư viện phức tạp. Dưới đây là danh sách ngắn những điều bạn cần trước khi bắt đầu:

- Một trình soạn thảo văn bản.
- Kiến thức về cách sử dụng terminal trên hệ thống của bạn.
- Đã cài đặt npm phiên bản 5.2 hoặc mới hơn (với việc phiên bản 5.2 đã xuất hiện từ tháng 7 năm 2017, khả năng cao là phiên bản npm của bạn đủ tốt nếu bạn đã có một phiên bản).
- Đã cài đặt một trình duyệt hiện đại (bất kỳ phiên bản gần đây của Edge, Firefox, Chrome hoặc Safari đều hoạt động).

Và đó là tất cả. Nếu bạn có thể đánh dấu được từng mục trong danh sách này, bạn đã sẵn sàng cho ví dụ đầu tiên này. Khi chúng ta đến các ví dụ khác trong các chương sau, bạn sẽ không cần nhiều hơn những gì có trong danh sách này.

1.4.1 The result
Dự án sẽ in ra một tiêu đề "Hello world!!!" (<h1>) trên một trang web. Hình 1.5 cho thấy nó sẽ trông như thế nào khi bạn hoàn thành (trừ khi bạn không nhiệt tình đến vậy và thích chỉ một dấu chấm than). 
 
Bạn sẽ chưa sử dụng JSX, chỉ là JavaScript thuần (thực sự, chúng ta sẽ không bắt đầu sử dụng JSX cho đến chương 3 và sau đó).

Learning React first without JSX
Mặc dù tất cả các nhà phát triển React viết mã React bằng JSX, trình duyệt chỉ chạy JavaScript tiêu chuẩn và không hiểu JSX trực tiếp. Đó là lý do tại sao việc có khả năng hiểu mã React trong JavaScript thuần rất hữu ích. Một lý do khác chúng tôi bắt đầu với JavaScript thuần là để cho thấy JSX là tùy chọn, mặc dù là ngôn ngữ mẫu tiêu chuẩn cho React. Cuối cùng, tiền xử lý JSX đòi hỏi một chút công cụ nâng cao, nhưng nó sẽ làm cho cả bộ thiết lập trở nên đơn giản hơn vì bạn sẽ thấy ít hơn về cách sản phẩm làm ra và làm thêm nhiều công việc thú vị hơn, đó là viết các thành phần React tuyệt vời.

Chúng tôi muốn giúp bạn bắt đầu với React càng sớm càng tốt mà không dành quá nhiều thời gian cho các thiết lập trong chương này. Bạn sẽ được giới thiệu cách bắt đầu một ứng dụng mới trong chương 2 và chúng tôi sẽ thêm JSX vào trong chương 3.

1.4.2 Writing the application

Dự án này đơn giản đến mức chỉ cần một tệp HTML duy nhất. Tệp này sẽ bao gồm các liên kết đến phiên bản mới nhất của React 18 (phiên bản ổn định nhất vào thời điểm viết) của thư viện React Core và ReactDOM. Tất nhiên, nó cũng sẽ bao gồm một chút mã JavaScript cần thiết để hiển thị ứng dụng rất đơn giản mà chúng tôi đang xây dựng.
Mã cho tệp HTML đơn giản và bắt đầu với việc bao gồm các thư viện trong `<head>`. Trong phần tử `<body>`, bạn sẽ tạo một container `<div>` với ID là root và một phần tử `<script>` (đó là nơi mã ứng dụng sẽ được thêm vào sau đó), như được hiển thị trong đoạn mã sau đây:


<!DOCTYPE html>
<html lang="en">
<head>
    <title>My First React Application</title>
    <!-- Imports the React library -->
    <script 
    src="//unpkg.com/browse/react@18.2.0/umd/react.development.js">
    </script>
    <!-- Imports the ReactDOM library -->
    <script 
    src="//unpkg.com/browse/react-dom@18.2.0/umd/react-dom.development.js">
    </script>
</head>
<body>
    <!-- Defines an empty <div> element để gắn kết với React UI -->
    <div id="root"></div>
    
    <script type="text/javascript">

    </script>
</body>
</html>

Chỉ cần gõ mã này bằng trình soạn thảo văn bản của bạn và lưu nó dưới dạng một tệp có tên là index.html trong một thư mục nào đó trên máy tính của bạn.
Bạn có thể tự hỏi tại sao chúng ta phải tạo một node <div> để render nội dung thay vì rendering phần tử React trực tiếp trong <body> elements. Câu trả lời là làm như vậy có thể dẫn đến xung đột với các thư viện và browser extensions khác nhau có thể thay đổi nội dung của tài liệu. Nếu bạn cố gắng gắn một phần tử trực tiếp vào `<body>`, bạn sẽ nhận lỗi console sau:
Warning: createRoot(): Creating roots directly with document.body is
➥ discouraged, ....
Điều này là một điều tốt khác về React: nó cung cấp cảnh báo và thông báo lỗi tốt!
LƯU Ý: React warning and error messages không phải là một phần của production build  để giảm tiếng ồn, tăng cường bảo mật và giảm kích thước phân phối.
Production build là tệp được tối giản hóa từ thư viện React Core, tức là react.min.js. Phiên bản phát triển với các cảnh báo và thông báo lỗi là phiên bản chưa được tối giản, react.development.js, như bạn thấy chúng tôi sử dụng trong ví dụ này.
Bằng cách bao gồm libraries trong tệp HTML, bạn có quyền truy cập vào các React and ReactDOM global objects:  window.React và window.ReactDOM. 
Bạn sẽ cần hai phương thức từ những đối tượng đó: một để tạo một element (React) và một phương thức khác để hiển thị nó trong đối tượng <div> container (ReactDOM), như bạn thấy trong danh sách 1.2. 

Để tạo một React element, bạn chỉ cần gọi React.createElement(elementName, data, children) với ba
đối số có ý nghĩa như sau:
- elementName : HTML tag dưới dạng chuỗi (ví dụ, 'h1') hoặc một custom component class dưới dạng object. Hiện tại chúng ta chưa có bất kỳ component tùy chỉnh nào, nhưng chúng ta sẽ bắt đầu tạo chúng trong chương 2.
- data: Một data object chứa các attributes và properties cho element. Hiện tại chúng ta không cần properties nào, nên chúng ta chỉ truyền vào null. Chúng ta sẽ quay lại sử dụng properties trong chương 2.
- children: Các child elements hoặc inner HTML/text content. Trong ví dụ này, đó chỉ là "Hello world!!!".
Listing 1.2 Creating and rendering an h1 element
<body>
    <!-- Defines an empty <div> element để gắn kết với React UI -->
    <div id="root"></div>
    
    <script type="text/javascript">
        // Creates an h1 React element with the text "Hello world!!!"
        const reactElement = React.createElement('h1', null, 'Hello world!!!');
        const domNode = document.getElementById('root');
        // Tạo root holder cho ứng dụng React được kết nối với DOM element cụ thể (domNode)
        const root = ReactDOM.createRoot(domNode);
        // Renders the h1 element into the root holder
        root.render(reactElement);
    </script>
</body>

Đoạn mã trong danh sách 1.2 được đặt trong thẻ `<script>` trong tệp HTML, mà bạn đã tạo
trước đó, vào chỗ của `...` mà ban đầu chúng ta đã đặt ở đó như một địa chỉ tạm. Danh sách này lấy một React element và lưu tham chiếu đến đối tượng này trong biến `reactElement`.
Biến ` reactElement ` không phải là một DOM node thực sự; thay vào đó, đó là một instantiation của
React h1 component (element). Bạn có thể đặt tên cho nó bất kỳ cách nào bạn muốn, ví dụ, hello-
WorldHeading.  Nói cách khác, React cung cấp một sự trừu tượng qua DOM.
Khi element được tạo ra và lưu trữ trong biến, sau đó bạn tạo một người giữ ứng dụng React React
application holder (gọi là root) từ phần tử DOM bằng cách sử dụng phương thức ReactDOM.createRoot().
Cuối cùng, bạn hiển thị React element vào root với phương thức root.render(), như được hiển thị trong danh sách 1.2.
Nếu bạn muốn, bạn có thể di chuyển tất cả các bước vào một cuộc gọi duy nhất. Kết quả là giống nhau,
ngoại trừ bạn không sử dụng ba biến phụ trợ, như chúng tôi đã làm trong danh sách tiếp theo.

Listing 1.3 Single statement
ReactDOM
     .createRoot(document.getElementById('root'))
     .render(React.createElement('h1', null, 'Hello world!!!'));

Chúng ta sẽ sử dụng phiên bản rõ ràng hơn trong danh sách 1.2, vì vậy tệp HTML đầy đủ
bây giờ sẽ trông như danh sách dưới đây.
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My First React Application</title>
    <!-- Imports the React library -->
    <script 
    src="//unpkg.com/browse/react@18.2.0/umd/react.development.js">
    </script>
    <!-- Imports the ReactDOM library -->
    <script 
    src="//unpkg.com/browse/react-dom@18.2.0/umd/react-dom.development.js">
    </script>
</head>
<body>
    <!-- Defines an empty <div> element để gắn kết với React UI -->
    <div id="root"></div>
    
    <script type="text/javascript">
        const reactElement = React.createElement(
            'h1', 
            null, 
            'Hello world!!!'
        );
        const domNode = document.getElementById('root');
        const root = ReactDOM.createRoot(domNode);
        root.render(reactElement);
    </script>
</body>
</html>

Với tệp HTML đã hoàn thành, bây giờ chúng ta cần xem nó hoạt động bằng cách phục vụ nội dung
đến trình duyệt của chúng ta.

1.4.3 Installing and running a web server

Bây giờ đến bước tiếp theo, serving the HTML page cho trình duyệt. Tại sao chúng ta cần phục vụ serve nội dung? Liệu chúng ta có thể mở trực tiếp tệp HTML trong trình duyệt không? Do hạn chế cross-origin, bạn không thể mở tệp nằm trên ổ cứng local của bạn trong trình duyệt và có nó truy cập nội dung trên các miền khác (như thư viện React được tải từ https://unpkg.com). Trình duyệt đơn giản không cho phép điều này. Bạn có thể thử mở tệp trực tiếp trong trình duyệt của bạn bằng cách nhấp đúp vào nó, nhưng nó sẽ chỉ hiển thị một trang trắng trống rỗng. Do đó, không thể thực hiện điều này.
Thay vào đó, chúng ta cần serve nội dung bằng cách sử dụng một local development web server. Điều này có vẻ phức tạp đến nỗi không tin nổi, nhưng thực sự rất đơn giản để thực hiện.
Nếu bạn đã thiết lập node theo khuyến nghị trong phần giới thiệu, điều này sẽ đủ để bạn bắt đầu. Chỉ cần nhập lệnh sau trong thư mục mà bạn đã lưu tệp index.html của mình:
$ npx serve
Đó là tất cả. Bạn có thể được hỏi để cài đặt một gói (nếu bạn chưa sử dụng lệnh này trước đây, đơn giản nhấn Enter để xác nhận), nhưng sau vài giây, khi công cụ báo cáo rằng mọi thứ đều đang diễn ra, máy chủ web của bạn đang chạy.

Local development web server
Rất tiếc là trong ví dụ đầu tiên này, bạn phải lo lắng về việc thiết lập local web server của riêng bạn. Mặc dù công việc này rất đơn giản, nhưng nó hơi phiền phức ở đây. Nếu vì một lý do nào đó mà lệnh đã cho không hoạt động với bạn, có một vài cách khác để dễ dàng serve thư mục hiện tại như một local web server.
Nếu bạn có Node, bạn có thể thử lệnh này:
$ npx http-server -p 3000
Hoặc nếu bạn có cài đặt Python 2 hoạt động trên máy tính của bạn, bạn chỉ cần thực hiện các bước sau:
$ python -m SimpleHTTPServer 3000
Hoặc nếu bạn có cài đặt Python 3 hoạt động, bạn có thể làm như sau (tùy thuộc vào cài đặt của bạn, bạn có thể phải nhập python3 thay vì python trong lệnh sau):
$ python -m http.server 3000
Cuối cùng, nếu bạn có cài đặt PHP và đang hoạt động cục bộ, bạn có thể làm như sau:
$ php -S localhost:3000
Bất kỳ lệnh nào trong số đó đều sẽ chạy một máy chủ web cục bộ trên máy tính của bạn tại thư mục bạn chạy lệnh, phục vụ tệp HTML của bạn tại http://localhost:3000.

1.4.4 Going to the local website
Với web server đang chạy, bạn có thể mở trình duyệt và truy cập vào trang web này:
http:/ /localhost:3000
Ở đây, bạn nên thấy ứng dụng của bạn đang hoạt động và nó sẽ trông khá giống như hình 1.5 ở đầu phần này.
Hình 1.6 hiển thị Elements tab trong browser developer tools với <h1>element được chọn. Bạn biết rằng React phải đã làm một cái gì đó ở đây vì trong tệp HTML nguồn của bạn, không có phần tử <h1> bên trong nút gốc - nó trống rỗng.
Chúc mừng! Bạn vừa triển khai ứng dụng React đầu tiên của mình!

 
Separate JavaScript file
Bạn có thể trừu tượng hóa mã JavaScript vào một tệp riêng biệt thay vì bao gồm mã nguồn trực tiếp trong tệp HTML (xem listing 1.1). Ví dụ, bạn có thể tạo một tệp có tên là script.js và sao chép và dán đoạn mã đầy đủ từ cả listing 1.2 hoặc listing 1.3 vào tệp đó. Sau đó, trong tệp HTML, bạn cần liên kết đến tệp script.js của bạn sau thẻ <div id="root"> thay vì bao gồm mã nguồn, như sau:
<div id="root"></div>
<script src="script.js"></script>
Từ chương tiếp theo trở đi, chúng ta sẽ không tạo các ứng dụng React của mình như vậy nữa. Chúng ta sẽ sử dụng một công cụ nhỏ để nhanh chóng tạo và thiết lập cơ bản cho ứng dụng React của chúng ta, điều này sẽ làm cho toàn bộ quá trình này trở nên mượt mà hơn. Nó sẽ chịu trách nhiệm về việc phục vụ nội dung của chúng ta nữa, vì vậy bạn không cần lo lắng về máy chủ web nữa.
1.5 Quiz
1 React là một framework đầy đủ và bạn có thể tạo nhiều ứng dụng chỉ bằng React. Đúng hay sai?
2 Vấn đề chính mà React giải quyết là gì?
a. Fetching data from the server
b. Creating beautiful HTML widgets
c. Rendering dynamic data in a UI layer
3 Các React components được hiển thị vào DOM bằng phương pháp nào sau đây? (Chú ý, đây là một câu hỏi khó!)
a. ReactDOM.appendRoot(...).render()
b. ReactDOM.renderRoot(...).render()
c. ReactDOM.createRoot(...).render()
d. ReactDOM.launchRoot(...).render()
4 Bạn phải sử dụng Node.js trên server để có thể sử dụng React trong ứng dụng SPA. Đúng hay sai?
5 Bạn phải bao gồm react-dom.js để render các React elements trên một trang web. Đúng hay sai?



Quiz answers
1 False. You almost always have to use other frameworks or libraries to create the
vast majority of React applications.
2 While you can create beautiful HTML widgets in React, the primary problem
that React solves is to render dynamic data in a UI layer (answer c).
3 ReactDOM.createRoot(...).render().
4 False. You can use any backend technology.
5 True. You need the ReactDOM library.

Summary
- React cho web bao gồm thư viện React Core và ReactDOM. React Core tập trung vào việc building and sharing composable UI có thể ghép lại bằng cách sử dụng JavaScript và, tùy chọn, JSX một cách phổ quát. Ngược lại, ReactDOM được sử dụng trong trình duyệt để hiển thị DOM và hiển thị từ phía máy chủ.
- React là declarative; chủ yếu hoạt động như một view or UI layer
- Các thành phần trong React được tạo ra bằng cách sử dụng `ReactDOM.createRoot()`.
- Phát triển React liên quan đến việc sử dụng JavaScript thuần để sáng tạo và sắp xếp UI.
- Mặc dù JSX là tùy chọn, nhưng nó là cú pháp rộng rãi được chấp nhận để tạo đối tượng React.
- React có thể tích hợp vào ngăn xếp web của bạn theo nhiều cách, từ một widget nhỏ trên một trang đến thành phần cơ bản của một trang web.
- React không phải là một framework toàn diện như Swiss Army knife; thay vào đó, nó hoạt động như UI layer của một ứng dụng web và thường được sử dụng kết hợp với các data libraries như Redux hoặc XState.

Chapter 2 – Baby steps with React
This chapter covers
 Creating a new React project
 Nesting elements
 Creating a component class
 Working with properties

Chương này sẽ hướng dẫn bạn cách tạo một dự án React mới và cách tạo các custom components để hiển thị HTML. Cả hai khái niệm này sẽ là cơ sở cho tất cả các chương sau này.
Đầu tiên, chúng ta sẽ xem xét cách tạo một dự án React mới. Trong quá trình làm điều này, chúng tôi sẽ hướng dẫn bạn cách bắt đầu các dự án React của riêng bạn và cách sử dụng hệ thống React template để nhanh chóng tạo các ví dụ và dự án mà chúng ta sẽ làm việc trong cuốn sách này. Thật kỳ diệu khi chỉ trong một dòng bạn có thể tải mã xuống và sẵn sàng chạy với tất cả mọi thứ được thiết lập cho bạn!

Khi chúng ta bắt đầu dự án React đầu tiên của mình, chúng tôi sẽ giới thiệu một số khái niệm cơ bản của React mà bạn sẽ sử dụng thường xuyên, bao gồm các elements, components và properties. Nói chung, các elements là các instances của các components có thể truyền properties. Sử dụng chúng để làm gì và tại sao bạn sử dụng chúng? Hãy chờ đến thông tin này cho đến khi chúng ta đến phần 2.3 vì, ngay bây giờ, chúng tôi sẽ thảo luận về cách tạo một ứng dụng web React mới.

NOTE: Mã nguồn cho các ví dụ trong chương này có sẵn tại https://rq2e.com/ch02. Tuy nhiên, ở phần 2.2, bạn sẽ biết rằng bạn không cần phải tải xuống bất cứ điều gì bằng cách thủ công. Bạn có thể khởi tạo tất cả các ví dụ từ chương này và các chương tiếp theo trực tiếp từ dòng lệnh bằng một lệnh duy nhất.
2.1 Creating a new React app

Trong phần này, chúng tôi sẽ giới thiệu cho bạn một chương trình command-line kỳ diệu sẽ giúp tất cả các cài đặt React của bạn diễn ra một cách mượt mà. Chỉ trong ba lệnh ngắn và vài phút, bạn sẽ tải xuống một ứng dụng web React giả mạo hoàn toàn hoạt động, compile nó, run nó thông qua một web server và xem nó trong browser của bạn (xem tổng quan trong hình 2.1).
 

Nếu bạn đã cài đặt một phiên bản hiện đại của Node (và npm) như được khuyến khích trong phần giới thiệu, bạn nên có thể viết lệnh sau trong terminal của bạn:
$ npx create-react-app name-of-app
LƯU Ý: "npx" không phải là một lỗi đánh máy. "npx" là một package runner tool đi kèm với npm. Nó cho phép chúng ta chạy các lệnh bằng cách sử dụng các gói chỉ có sẵn trong thư mục dự án này và/hoặc chạy các lệnh sẽ được tải xuống động khi cần thiết.

Chạy lệnh này và một ứng dụng React mới sẽ được thiết lập cho bạn! Lần đầu tiên bạn chạy lệnh này, npm sẽ yêu cầu xác nhận để tải xuống create-react-app tool (chỉ cần nhấn Enter để xác nhận). Điều này liên quan đến các bước 1.a và 1.b trong hình 2.1. Mỗi khi bạn sử dụng lệnh sau đó, không có câu hỏi nào sẽ được đặt.
LƯU Ý: Chúng tôi sẽ gọi create-react-app tool là CRA trong các phần sau.

Lệnh này sẽ tạo ra một folder mới với tên được truyền vào, đó là name-of-app trong trường hợp trước đó. Bên trong folder này, tiện ích sẽ khởi tạo một Git project mới, tải xuống các tài nguyên resources cần thiết cho ứng dụng, sau đó tải xuống và cài đặt địa phương tất cả các phụ thuộc cần thiết cho dự án.
Lệnh sẽ chạy trong một khoảng thời gian ngắn, có thể khoảng 1-3 phút tùy thuộc vào độ phức tạp của dự án và điều kiện mạng. Khi lệnh hoàn tất, bạn sẽ thấy một cái gì đó như sau:
Success! Created name-of-app at <folder>
Inside that directory, you can run several commands
npm start		[1]
Starts the development server.
npm run build
Bundles the app into static files for production.

npm test
Starts the test runner.

npm run eject
Removes this tool and copies build dependencies, configuration
files and scripts into the app directory. If you do this, you
can't go back!

We suggest that you begin by typing:
cd name-of-app
npm start		[1]

Happy hacking!	[2]

1.	Đây là một trong bốn lệnh mà bạn có thể chạy trong ứng dụng của mình (chúng tôi sẽ thảo luận về nó tiếp theo).
2.	Tại sao vậy, cảm ơn bạn—và cầu mong việc hack của bạn mãi mãi là mũ trắng!

Ồ, thú vị. Lưu ý rằng nếu đầu ra của bạn đề cập đến một lệnh có tên là yarn thay vì npm, đừng lo lắng. Hãy xem phần bên cạnh để có một giải thích.
npm alternatives
Có nhiều trình quản lý gói phổ biến cho các dự án JavaScript hoạt động trên cùng một kho lưu trữ và cấu trúc gói, nhưng với các lệnh khác nhau một chút. Trình quản lý phổ biến nhất là npm, nhưng có các lựa chọn khác bao gồm Yarn và pnpm. Trình quản lý phổ biến, npm, được cài đặt sẵn với Node và là trình quản lý mặc định mà nhiều người sử dụng.
Tuy nhiên, bạn có thể chọn cài đặt một trình quản lý khác, có cấu trúc lệnh đơn giản hơn một chút. Đối với mục đích của cuốn sách này, không có sự khác biệt giữa việc sử dụng npm hoặc một lựa chọn khác, ngoại trừ một số cú pháp khác nhau khi nhập lệnh. Nếu bạn có Yarn hoặc pnpm, có khả năng bạn cũng đã cài đặt npm, vì vậy điều đó có lẽ sẽ luôn hoạt động cho bạn.
Nếu bạn muốn sử dụng một trong những trình quản lý gói này, hãy kiểm tra tài liệu hướng dẫn về cách chạy các lệnh:
- Yarn: https://classic.yarnpkg.com/lang/en/docs/cli/run/
- pnpm: https://pnpm.io/cli/run

Bây giờ, hãy tuân thủ đề xuất trong đoạn mã trước và chạy hai lệnh sau:
$ cd name-of-app
$ npm start
Bây giờ phần thứ ba của phép màu xảy ra. Một máy chủ phát triển React được khởi động, biên dịch tất cả các tệp và tài nguyên được sử dụng (hành động 3.a trong hình 2.1) và khởi chạy một máy chủ phát triển web cục bộ (hành động 3.b trong hình 2.1). Sau vài giây, dòng lệnh sẽ hiển thị một cái gì đó như sau:
Compiled successfully!
You can now view name-of-app in the browser.
Local: http://localhost:3000
Hơn nữa, ứng dụng cũng đã được mở trong trình duyệt của bạn, vì lệnh cũng mở một cửa sổ trình duyệt ở URL chính xác (hành động 3.c trong hình 2.1). Nếu không, đơn giản mở localhost:3000 trong trình duyệt để xem ứng dụng. Cửa sổ trình duyệt này sẽ hiển thị một ứng dụng React (như được thể hiện trong hình 2.2) đã được tạo cho bạn bằng một template. Đây là template mặc định được sử dụng cho các React applications mới không chỉ định một template cụ thể để sử dụng. Chúng ta sẽ thảo luận về template một chút sau trong phần 2.1.3.
 
Lưu ý rằng lệnh cuối cùng này, `npm start`, là một lệnh chạy liên tục ở terminal. Nó sẽ theo dõi các tệp nguồn của bạn, biên dịch lại toàn bộ ứng dụng khi có bất kỳ thay đổi nào trong tệp nguồn, và thậm chí là tải lại trình duyệt với ứng dụng được cập nhật (hành động 4–4.d trong hình 2.1)! Đó là thật sự là phép màu.
Khi bạn muốn hủy lệnh này, đơn giản nhấn Ctrl-C trong terminal của bạn, và bạn sẽ quay lại dấu nhắc terminal thông thường. Tuy nhiên, ứng dụng của bạn sẽ không còn hoạt động vì bạn cũng đã dừng local development web server.
Bạn có thể đã chú ý rằng đầu ra trước đó từ việc tạo ứng dụng của chúng ta liệt kê không chỉ lệnh bắt đầu mà chúng ta vừa sử dụng mà còn ba lệnh khác: build, test và eject. Chúng tôi sẽ đi sâu vào cả bốn lệnh này chi tiết hơn trong phần tiếp theo.

2.1.1 React project commands

Bây giờ khi bạn có mã nguồn ứng dụng React này có sẵn trên hệ thống của mình, bạn có thể muốn tương tác với nó theo nhiều cách. Hai điều chính bạn muốn là xem những gì bạn đang phát triển trong quá trình phát triển và triển khai ứng dụng của bạn lên một máy chủ web. Bạn cũng có thể muốn chạy tất cả các bài test trong ứng dụng của bạn để xác minh rằng mọi thứ vẫn hoạt động theo thiết kế. Cuối cùng, bạn có thể muốn thoát khỏi ranh giới của CRA để nghịch với hệ thống bên dưới. CRA trừu tượng hóa một số điều mà bạn không cần phải lo lắng lúc đầu, nhưng khi ứng dụng trở nên phức tạp hơn, bạn có thể muốn truy cập vào cấu hình ứng dụng của mình. Đối với bốn mục đích này, một ứng dụng React mới được tạo ra bằng CRA đi kèm với bốn lệnh sau:

 start: Khởi chạy một local development web server và liên tục biên dịch dự án khi có sự thay đổi, phục vụ nó cho bất kỳ trình duyệt cục bộ nào.
 build: Biên dịch tất cả các tài nguyên thành một package sẵn sàng cho sản xuất có thể triển khai lên máy chủ web đúng.
 test: Khởi chạy một chương trình chạy thử nghiệm test runner sẽ chạy tất cả các bài unit tests được định nghĩa trong dự án của bạn.
 eject: Hiển thị cách dự án hoạt động bên trong và làm cho nó hoàn toàn có thể cấu hình.

Hãy đi qua chúng một cách chi tiết và thảo luận về cách và khi nào sử dụng chúng.
START
Lệnh start là lệnh chính của bạn, là lệnh bạn sử dụng mỗi khi bạn bắt đầu một dự án mới hoặc tiếp tục một dự án cũ để bắt đầu làm việc lại. Ở đầu phiên lập trình của bạn, bạn sẽ chạy lệnh start trong terminal, sau đó bạn sẽ sẵn sàng mã hóa trong trình soạn thảo của bạn trong khi nội dung được cập nhật tự động trong trình duyệt của bạn.
Lệnh start sẽ xây dựng dự án của bạn ở nền liên tục bằng cách sử dụng phiên bản phát triển của React và các thư viện tiện ích của nó. Điều này khác biệt từ phiên bản sản xuất của React được sử dụng trong lệnh build. Phiên bản phát triển của React bao gồm thông báo lỗi và cảnh báo tốt hơn cũng như các tùy chọn để gỡ lỗi ứng dụng khi nó đang chạy trong trình duyệt. Tuy nhiên, phiên bản phát triển của React cũng lớn hơn rất nhiều về kích thước tệp, vì vậy bạn không muốn xuất bản ứng dụng của mình bằng phiên bản này. Nó sẽ làm cho ứng dụng của bạn trở nên lớn không cần thiết và làm chậm người dùng cố gắng truy cập nó.
Lệnh start cũng sẽ tải lại ứng dụng trong trình duyệt khi nó đang chạy, nhưng theo cách thông minh hơn so với việc tải lại toàn bộ cửa sổ trình duyệt. React sẽ cố gắng tải lại chỉ các phần logic liên quan đã thay đổi và nếu không, nó sẽ giữ nguyên ứng dụng. Ví dụ, nếu bạn đã nhấp vào một nút để thu gọn một phần sẽ mở mặc định khi ứng dụng khởi chạy, React sẽ có thể chèn mã cập nhật trong khi vẫn giữ trạng thái trong trình duyệt, để phần này vẫn thu gọn trong khi logic khác được cập nhật.
BUILD
Đây là lệnh để chạy khi bạn đã sẵn sàng xem ứng dụng của mình được triển khai lên một máy chủ web thực và để người dùng thử nghiệm. Khi bạn chạy lệnh build, bạn sẽ sử dụng phiên bản sản xuất của React, có kích thước nhỏ hơn và được tối ưu hóa cho triển khai. Kết quả của lệnh build sẽ được đặt trong thư mục /build.
Mặc định, không có gì khác xảy ra nhiều, nhưng nếu bạn muốn, bạn cũng có thể thiết lập triển khai trực tiếp lên cloud web hosting  solution của bạn trong lệnh build nếu bạn muốn. Kiểm tra tài liệu của nhà cung cấp dịch vụ lưu trữ cloud web để biết cách làm điều này. Chúng tôi sẽ không sử dụng lệnh này trong cuốn sách này, vì chúng tôi sẽ sử dụng một template khác để triển khai ứng dụng trong dự án nơi triển khai lên đám mây sẽ là một lựa chọn.

TEST
Nếu bạn muốn chạy tất cả các bài unit tests được định nghĩa trong dự án của bạn, hãy chạy lệnh này. Bạn có thể làm điều đó trên template mặc định trống rỗng cũng vì template mặc định đã có một tệp kiểm thử mặc định.

EJECT
Lệnh này có thể nguy hiểm một chút vì nó không thể đảo ngược. Nếu bạn eject ứng dụng của mình, bạn sẽ có quyền truy cập vào nhiều tùy chọn có thể cấu hình bên trong thiết lập React hơn là khác, nhưng bạn cũng mất khả năng cập nhật tự động lên các phiên bản mới của tất cả các công cụ liên quan. Chúng tôi sẽ không bao gồm việc eject ứng dụng của bạn trong cuốn sách này, nhưng chúng tôi sẽ thảo luận về nó một cách ngắn gọn hơn trong phần 2.1.4 khi xem xét các ưu và nhược điểm.

2.1.2 File structure

Khi bạn tạo một dự án với CRA, nó hầu như luôn tuân theo cùng một cấu trúc tệp. Custom templates có thể thực hiện các điều khác nhau, nhưng thường ít khi làm vậy. Cấu trúc bao gồm những phần quan trọng sau:
/
  public/
    index.html
  src/
    index.js
    App.js
  package.json

1. public folder: Được sử dụng cho các files sẽ được served trực tiếp thông qua web server. Bao gồm tệp index.html serves toàn bộ ứng dụng của bạn cũng như các tệp nhị phân bạn không muốn gói vào ứng dụng của mình, chẳng hạn như nội dung được yêu cầu bởi tệp index.html trực tiếp (ví dụ: favicon, Cascading Style Sheets [CSS], fonts, hoặc hình ảnh để chia sẻ) và các tệp lớn (ví dụ: video và hình ảnh).
2. src folder: Nơi mà toàn bộ JavaScript được gói vào cũng như bất kỳ nội dung khác nào bạn muốn gói thành một package duy nhất. Điều này chủ yếu chỉ là JavaScript, nhưng cũng có thể bao gồm CSS, icons, small images, JSON files, và nhiều hơn nữa. Quá trình gói bundling đó bắt đầu từ tệp index.js bên trong thư mục src. Thông thường, ứng dụng chính sẽ nằm trong một tệp có tên là App.js hoặc app.js, phụ thuộc vào sự ưa thích cá nhân, nhưng ngoại trừ điều này, bạn có thể linh hoạt ở đây. Một số templates sắp xếp nội dung bên trong thư mục src theo các thư mục con, điều này là cần thiết để tổ chức dự án lớn hơn.
3. package.json: Tệp cấu hình chính cho dự án của bạn, như yêu cầu bởi npm và Yarn. Đây là file starting cho dự án của bạn và defines the dependencies cũng như các lệnh bạn có thể chạy, như đã đề cập trong phần 2.1.1.

The root folder thường chứa nhiều configuration files khác nhau được yêu cầu cho các thư viện khác nhau được bao gồm trong dự án. Không hiếm thấy khi thấy các template tùy chỉnh với 20+ tệp cấu hình khác nhau tại thư mục gốc của dự án. Bây giờ, hãy tiếp tục để tìm hiểu về các template tùy chỉnh là gì và chúng làm thế nào để giúp bạn.
2.1.3 Templates
Mặc dù ứng dụng mặc định mà chúng ta thấy trong hình 2.2 khá tốt, nhưng nó không phải lúc nào cũng hữu ích. Ứng dụng mặc định giúp bạn tạo một ứng dụng web đơn giản theo cùng kiểu như cách ứng dụng web được tạo ra, nhưng có thể đó không phải là điều bạn đang tìm kiếm. Nếu bạn muốn tạo một ứng dụng web sử dụng một ngăn xếp công nghệ cụ thể hoặc sử dụng React theo một cách cụ thể, bạn có thể muốn sử dụng một different starting template để thiết lập môi trường phát triển của bạn đúng cách.

Khi bạn sử dụng CRA, bạn có thể chỉ định một template để sử dụng. The default template là template bạn đã thấy trước đó với biểu tượng React (quay). Nếu bạn muốn chỉ định một template khác, bạn có thể làm như sau:
$ npx create-react-app name-of-app --template name-of-template
Bạn chỉ có thể sử dụng name of a template đã tồn tại; nếu nó không tồn tại, ứng dụng sẽ bị hủy. Thường, mọi người không phiền với việc chọn template và chỉ làm việc với template mặc định. Nhưng nếu bạn biết bạn muốn một thiết lập cụ thể hoặc muốn bắt đầu mã nguồn của mình từ một trạng thái nhất định, bạn có thể sử dụng một template để thiết lập môi trường phát triển của bạn đúng như bạn mong muốn. Một số template phổ biến bao gồm:

- --template minimal: Có ít tính năng hơn so với template mặc định, ví dụ, `--template minimal`. template này không bao gồm mages, CSS, tests, web vitals , và những điều nhỏ nhẹ khác được sử dụng trong template mặc định.

- --template typescript hoặc --template minimal- --template minimal-typescript Điều này hữu ích để bắt đầu một dự án mới sử dụng TypeScript.

- **Các thiết lập boilerplate phức tạp:** Được tạo ra bởi các nhà phát triển khác, nơi bạn đã có một ngăn xếp các phụ thuộc nhất định đã được tích hợp vào ứng dụng mới của bạn, ví dụ, --template redux-typescript, đi kèm với Redux và TypeScript, hoặc --template rb, một template React phổ biến (do đó là rb), đi kèm với nhiều thư viện uy tín khác nhau, bao gồm Redux với Redux-Saga, styled components, ESLint, husky và nhiều thứ khác.

Một trong những điều rất hữu ích về hệ thống template cho CRA là nó hoàn toàn phi tập trung. Bất kỳ ai cũng có thể xuất bản một gói lên npm và tổ chức nó một cách cho phép bạn sử dụng nó như một cơ sở cho các ứng dụng của bạn. Điều này, tất nhiên, cũng là một trong những hạn chế. Nếu bạn tìm thấy một template trên npm, không có cách nào nói liệu nó có tốt không hoặc thậm chí có thực hiện điều mà nó nói. Ở đây, bạn có thể tin tưởng vào sự khôn ngoan của đám đông - nếu nó phổ biến, có thể là nó tốt.

Một trong những lợi ích của việc cho phép hầu hết các nhà phát triển ngẫu nhiên đăng xuất một template lên npm là đó bao gồm cả chúng tôi, tác giả của cuốn sách này. Chúng tôi sẽ sử dụng các template React tùy chỉnh cho tất cả các ví dụ và dự án trong cuốn sách này. Chúng ta sẽ quay lại vấn đề này trong một giây. Trước tiên, chúng ta sẽ thảo luận về ưu và nhược điểm của việc sử dụng CRA.

2.1.4 Pros and cons

CRA (Create React App) mang lại nhiều lợi ích khi tạo một ứng dụng React mới, nhưng , như mọi công cụ khác, những lợi ích này đi kèm với những hậu quả. Chúng ta đã thảo luận về nhiều lợi ích, nhưng hãy liệt kê chúng ở đây:
- **Đơn giản:** Bạn ít phải lo lắng khi thiết lập một ứng dụng mới. Bạn nhận được quá trình biên dịch JavaScript XML (JSX), đóng gói bundling, testing, automatic reloading và nhiều tính năng khác mà không cần xử lý tất cả các sự phụ thuộc phức tạp.
- **Khả năng nâng cấp:** Bạn có thể dễ dàng nâng cấp lên các phiên bản mới của React và tất cả các thư viện khác. Chúng ta chưa thảo luận về cách thực hiện điều này, nhưng nó đơn giản bất ngờ. Chỉ cần chạy `npm install --exact react-scripts@VERSION` để nâng cấp toàn bộ dự án của bạn lên phiên bản cụ thể của React scripts. Kiểm tra hướng dẫn thay đổi cho react-scripts để biết chi tiết.
- **Cộng đồng:** Với số lượng lớn templates CRA và con đường dễ dàng để tạo thêm, bạn có thể luôn tìm thấy một templates đã làm trước với sự kết hợp đúng đắn của công cụ để bạn không phải đối mặt với việc pha trộn chúng đúng cách.
- **Tùy chỉnh:** Ngoài các mẫu khác nhau, bạn vẫn có khả năng thêm tất cả các plugin và thư viện khác bạn cần cho dự án của mình. Dự án của bạn liên kết, ví dụ, với cả Google Maps và Amazon Web Services (AWS)? Chỉ cần thêm thư viện của họ và bạn nên sẵn sàng hoạt động.

Tuy nhiên, cũng có một số hạn chế. Một số trong số đó có thể được bỏ qua, nhưng trong một số tình huống, bạn phải tìm kiếm các thiết lập khác ngoài những gì CRA có thể cung cấp. Chúng ta sẽ đề cập đến một số tình huống này ở đây:
- **Hiểu biết:** Nếu không thiết lập toàn bộ dự án từ đầu, bạn sẽ không biết tất cả những gì đang diễn ra trong một dự án như vậy. Nếu bạn đặt mình trong tình huống cần một thiết lập duy nhất nhưng luôn tin dùng vào CRA, bạn có thể nhanh chóng cảm thấy mình lạc lõng vì bạn thực sự không chú ý đến nó. Nhưng đó là sự đối lập của mọi sự trừu tượng: bạn đạt được lợi ích của việc không lo lắng nhưng phải trả giá bằng việc không biết chính xác điều gì đang xảy ra phía dưới.
- **Kiểm soát:** Bạn mất kiểm soát về thư viện nào được sử dụng. CRA hiện đang sử dụng webpack và BabelJS cho JSX bundling & biên dịch transpiling, nhưng chúng không phải là những "người chơi duy nhất" xung quanh. Gần đây, đã xuất hiện các công cụ như esbuild, Bun, SWC và Rome mà một phần bao phủ cùng lãnh thổ, nhưng bạn không thể dễ dàng chuyển sang một trong những công cụ đó. Bạn bị ràng buộc bởi bộ công nghệ mà CRA hiện đang chọn cho bạn. Tuy nhiên, đó cũng là một ưu điểm vì khi một công cụ khác trở thành tiêu chuẩn và có thể thậm chí là xuất sắc hơn Babel, CRA sẽ thích nghi và sử dụng công cụ đó thay vì bạn phải lo lắng về nó. Đối với những trường hợp bạn yêu cầu sử dụng một ngăn xếp cụ thể, bạn phải thiết lập dự án của mình từ đầu. Một lựa chọn khác là "eject" ứng dụng của bạn như mô tả trong phần 2.1.1, điều này mang lại khả năng cấu hình và kiểm soát bổ sung với chi phí là mất khả năng nâng cấp.
- **Tích hợp:** Nếu bạn muốn tích hợp ứng dụng của mình vào một thiết lập trên phía máy chủ, CRA hiện tại không thể giúp bạn. Đối với các dự án dựa trên các frameworks trang web như mô tả trong chương đầu tiên, bạn phải sử dụng các thiết lập do các frameworks đó cung cấp thay vì CRA.
Sau khi cân nhắc lợi và hại đã liệt kê, chúng tôi kết luận rằng CRA là lựa chọn hoàn hảo cho các nhà phát
 triển mới. Bạn có được sự đơn giản và ít lo lắng. Khi bạn có thêm kinh nghiệm, bạn có thể bắt đầu thử nghiệm bên ngoài CRA. Đó là lý do tại sao chúng tôi đã sử dụng CRA cho các ví dụ và dự án trong cuốn sách này.

2.2 A note about the examples in this book

Như đã đề cập, chúng tôi sẽ sử dụng CRA cho tất cả các dự án và hầu hết các ví dụ trong cuốn sách này. Điều duy nhất ngoại lệ là ví dụ đầu tiên bạn đã hoàn thành trong chương đầu tiên. Tất cả các templates chúng tôi đã tạo cho cuốn sách này sẽ được đặt tên theo cấu trúc sau:
rqXX-NAME 
Tất nhiên, rq đề cập đến React Quickly. XX sẽ được thay thế bằng số chương, và phần cuối cùng sẽ là một tên ngắn tùy chỉnh cho mỗi ví dụ. Đối với mỗi ví dụ và dự án sử dụng CRA, bạn sẽ thấy tên mẫu và cách sử dụng nó trong một sidebar như sau:
Repository: rq02-nesting
Ví dụ này có thể được xem trong repository rq02-nesting. Bạn có thể sử dụng repository  đó bằng cách tạo một ứng dụng web mới dựa trên mẫu liên quan:
$ npx create-react-app rq02-nesting --template rq02-nesting
Hoặc, bạn có thể truy cập trang web này để duyệt mã nguồn, xem ứng dụng hoạt động trực tiếp trong trình duyệt của bạn hoặc tải mã nguồn dưới dạng tệp zip:
[https://rq2e.com/rq02-nesting](https://rq2e.com/rq02-nesting)

Đôi khi, các ví dụ sẽ chứa nhiều biến thể multiple variants của mã nguồn, và trong những trường hợp như vậy, mỗi variants sẽ đi kèm với một template của riêng nó như vừa được hiển thị. Cũng có những ví dụ đi kèm với gợi ý cho bài tập thêm extra homework. Trong những trường hợp đó, một template sẽ được chỉ định làm điểm khởi đầu cho extra homework, và một template khác sẽ chứa một giải pháp có thể cho bài tập đó. Bạn có thể sử dụng solution template như nguồn cảm hứng hoặc để so sánh với giải pháp của bạn. Tất cả những bài tập này có thể có vô số solutions, vì vậy chỉ vì công việc của bạn không khớp với template không có nghĩa là nó sai - nó chỉ là khác biệt.
Để thuận tiện, bạn có thể thường sử dụng tên mẫu làm tên ứng dụng của mình. Vì vậy, giả sử bạn muốn bắt đầu làm việc trên ví dụ tiếp theo trong cuốn sách này. Tên template là rq02-nesting, vì vậy hãy sử dụng nó làm tên ứng dụng web:
$ npx create-react-app rq02-nesting --template rq02-nesting
Chỉ cần nhập điều đó vào cửa sổ console của bạn, và bạn đã sẵn sàng để bắt tay vào ví dụ để giải quyết vấn đề cùng với chúng tôi nếu bạn muốn. Bạn cũng có thể chỉ đọc chương và xem mã nguồn trong các danh sách trong sách. Nếu bạn thấy một số điều lạ hoặc cần đưa ngón tay vào mã để thử một số thứ, bạn có thể khởi tạo các mẫu và xem ví dụ trong thực tế. Bây giờ hãy tiếp tục với ví dụ này, mà có vẻ liên quan đến việc lồng vào một cái gì đó.

2.3 Nesting elements

Trở lại việc tạo ứng dụng React, đó là điều chúng ta đã đặt ra làm trong cuốn sách này, hãy bắt đầu làm mọi thứ trở nên phức tạp hơn một chút so với ví dụ giảng dạy đơn giản mà chúng ta đã xem xét trong chương 1. Trong chương đó, bạn đã học cách tạo một single React element. Như một lời nhắc, phương thức bạn sử dụng là React.createElement(). 
Ví dụ, bạn có thể tạo một phần tử liên kết link element như sau:

const reactLinkElement = React.createElement(
    "a", 
    { href: "http://react.dev" },
    "React Website"
)

Điều này là tốt miễn là chúng ta chỉ tạo một phần tử duy nhất. Vấn đề là mọi trang web đều có nhiều hơn một phần tử; nếu không, làm thế nào bạn có thể có bất kỳ thông tin nào khác ngoài một đoạn văn duy nhất?
Giải pháp cho việc tạo các cấu trúc đa phần tử theo cách phân cấp là nhúng các phần tử. Trong chương trước, bạn đã triển khai mã React đầu tiên của mình bằng cách tạo một phần tử React đơn và hiển thị nó trong DOM với ReactDOM.createRoot().render():
const title = React.createElement("h1", null, "Hello world!");
const domElement = document.getElementById("root");
ReactDOM.createRoot(domElement).render(title);

Chú ý rằng ReactDOM.createRoot().render() chỉ có thể nhận một single (root) React element làm đối số, đó là reactElement trong ví dụ này. Ứng dụng kết quả được hiển thị trong hình 2.3.

 

Repository: rq02-nesting
Ví dụ này có thể được xem trong repository rq02-nesting. Bạn có thể sử dụng repository  đó bằng cách tạo một ứng dụng web mới dựa trên mẫu liên quan:
$ npx create-react-app rq02-nesting --template rq02-nesting
Hoặc, bạn có thể truy cập trang web này để duyệt mã nguồn, xem ứng dụng hoạt động trực tiếp trong trình duyệt của bạn hoặc tải mã nguồn dưới dạng tệp zip:
[https://rq2e.com/rq02-nesting](https://rq2e.com/rq02-nesting)
Khi bạn check out template rq02-nesting, bạn sẽ có ứng dụng trước đó, nhưng lần này sử dụng CRA thay vì thêm thư viện và viết HTML bằng cách thủ công như chúng ta đã làm trong chương 1.
Hãy nhớ rằng khi bạn sử dụng createElement, đối số thứ ba là child of the element. Trong trường hợp này, chúng tôi chỉ cung cấp text đơn giản làm child. Nhưng text đó thực sự là một element khác ít nhất trong DOM kết quả. Trong React, nó không có một loại phần tử cụ thể, nhưng nó vẫn hoạt động như một phần tử đến một mức độ nào đó. Chúng ta có thể hiển thị mối quan hệ này trong một biểu đồ rất đơn giản, như được hiển thị trong hình 2.4.
 
2.3.1 Node hierarchy

Trước khi chúng ta xem cách tạo các cấu trúc HTML phức tạp complex HTML structures,, chúng ta cần một chút thuật ngữ cơ bản trước. HTML document thường được biểu diễn dưới dạng một cây ngược, như được hiển thị trong hình 2.5. Các Nodes trong cây thường được mô tả theo cách mô tả trong một gia đình (parent, child, v.v.).
 


Các thuật ngữ sau liên quan đến cấu tree structure:
- **Node:** Mọi thành viên trong cây đều là một node, bao gồm cả các phần tử HTML và các node văn bản. Tất cả các hộp trong hình 2.5 đều là các node. Hai hộp dưới cùng nhất là các node văn bản, và tất cả các hộp khác đều là các node phần tử.

- **Root:** Node đầu tiên (ở trên cùng) là root của tree. Trong hình 2.5, node <html> là root node.

- **Parent:** Node ngay phía trên một node cụ thể là cha của nó. Mỗi node trong cây chỉ có một parent. Node phía trên đó có thể được gọi là grandparent, và cứ tiếp tục như vậy. Trong hình 2.5, node cha của <body> là node <html>. The root node doesn’t have a parent, và nó là duy nhất một node trong cây không có cha.

- **Child:** Bất kỳ node nào ngay phía dưới một node cụ thể đều là con của node đó. Một node có thể có nhiều con. Các con của node <section> là các node <h1>, <p>, và <img>. Không phải tất cả các node đều có con. Phần tử <img> không có con. Text nodes never have children.

- **Sibling (Anh em ruột):** Hai node có cùng một cha được coi là anh em ruột. The <p> node has two sibling nodes: the <h1> and <img> nodes.
- **Ascendants (Tổ tiên):** Cha của một node, cha của nó, cha của cha của nó, và cứ tiếp tục đến gốc được gọi là tổ tiên của một node. Node <h1> có ba tổ tiên: các node <section>, <body>, và <html>.

- **Descendants (Hậu duệ):** Các con của một node, tất cả con của chúng, tất cả con của con của chúng, và cứ tiếp tục như vậy được gọi là hậu duệ của một node. The <section> node has five descendants: ba con trực tiếp cũng như hai node văn bản là cháu của hai con đầu tiên.

- **Nesting (Lồng ghép):** Lồng ghép là quá trình sắp xếp các node trong một cây và quyết định node nào sẽ là con của node nào, tạo ra document tree. Trong hình 2.5, chúng ta đã quyết định lồng ghép các node <h1>, <p>, và <img> bên trong node <section>.

2.3.2 Simple nesting

Hãy giả sử bạn muốn hiển thị từ "world" in nghiêng trong chuỗi "Hello world!" nhưng vẫn đặt nó trong một phần tử h1. Như được thể hiện trong hình 2.6, bạn tạo một phần tử em với chuỗi "world" làm con và một phần tử h1 khác với ba con:
 
- Chuỗi "Hello " (lưu ý khoảng trắng ở cuối)
- Phần tử em từ trước
- Chuỗi "!"
Như bạn có thể thấy ở đây, chúng ta đang truyền năm arguments vào createElement: đầu tiên là element type, sau đó là các properties, và cuối cùng là các phần tử con của phần tử. Bạn có thể truyền bao nhiêu đối số làm con cho một element tùy thích. Bạn cũng có thể truyền các phần tử con dưới dạng một mảng:

const title = React.createElement("h1", null, ["Hello ", world, "!"])

Trong trường hợp này, không có lý do gì phải đặt các phần tử vào một mảng trước khi truyền chúng như một đối số, nhưng nếu chúng ta đã có một mảng các phần tử, chúng ta có thể truyền nó làm một đối số mà không cần một mảng bao ngoài. Kết hợp tất cả lại (không sử dụng một mảng), đoạn mã hoàn chỉnh trở thành đoạn mã như sau.

const world = React.createElement("em", null, "world");
const title = React.createElement("h1", null, "Hello ", world, "!");
const domElement = document.getElementById("root");
ReactDOM.createRoot(domElement).render(title);

Nếu chúng ta thực hiện điều này, chúng ta sẽ có ứng dụng của mình trông giống như trong hình 2.7 trên trình duyệt.

Repository: rq02-nesting-italic
This example can be seen in repository rq02-nesting-italic. You can use that
repository by creating a new web app based on the associated template:
$ npx create-react-app rq02-nesting-italic --template rq02-nesting-italic
Alternatively, you can go to this website to browse the code, see the application in
action directly in your browser, or download the source code as a zip file:
https://rq2e.com/rq02-nesting-italic
2.3.3 Siblings

Trong nhiều trường hợp, bạn chỉ có thể sử dụng một đối tượng React duy nhất ở cấp độ cao nhất. Điều này áp dụng cho phương thức `ReactDOM.createRoot().render()` — chỉ có thể render một đối tượng duy nhất vào DOM như là đối tượng root. Bạn cũng sẽ thấy cách các thành phần tùy chỉnh chỉ có thể trả về một đối tượng duy nhất một chút sau.
Nhưng nếu bạn muốn hiển thị một tiêu đề headline and sau đó là một link sau nó trong ví dụ của chúng ta trước đó (xem hình 2.8)? Đó sẽ là hai đối tượng khác nhau đứng cạnh nhau, và bạn không thể render chúng trực tiếp bằng cách sử dụng `ReactDOM.createRoot().render()`.
 
Thay vào đó, bạn phải bọc chúng trong một đối tượng khác (một cái gì đó thay thế cho ? trong hình 2.8). Bạn có hai lựa chọn khác nhau ở đây. Một lựa chọn là sử dụng một DOM element trung lập, điều này đơn giản, nhưng sẽ thêm một phần tử "vật lý" vào HTML đầu ra. Sự lựa chọn thay thế là sử dụng một đối tượng React Fragment, hoạt động giống như bất kỳ phần tử nào khác, nhưng không tạo ra bất kỳ HTML đầu ra nào. Xem sự khác biệt giữa các cách tiếp cận này trong hình 2.9. 
Nếu bạn muốn sử dụng một DOM element trung lập, bạn có thể, ví dụ, sử dụng một `<div>` để nhóm chúng như được hiển thị trong đoạn mã sau. Điều này dẫn đến HTML bạn thấy trong hình 2.10.
Listing 2.2 Two elements in a grouping container
const title = React.createElement("h1", null, "Hello world!");
const link = React.createElement("a", { href: "http://react.dev"}, "Read more");
const group = React.createElement("div", null, title, link);
const domElement = document.getElementById("root");
ReactDOM.createRoot(domElement).render(group);

	
 
Repository: rq02-siblings-div
This example can be seen in repository rq02-siblings-div. You can use that
repository by creating a new web app based on the associated template:
$ npx create-react-app rq02-siblings-div --template rq02-siblings-div
Alternatively, you can go to this website to browse the code, see the application in
action directly in your browser, or download the source code as a zip file:
https://rq2e.com/rq02-siblings-div
Phần tử `<div>` thường là một lựa chọn tốt cho block-level content, và `<span>` được sử dụng cho inline-level content. Nhưng bạn không cần phải sử dụng một phần tử " real” .Bạn cũng có thể tạo một phần tử React trống, mục đích duy nhất của nó là nhóm nhiều phần tử khác và không xuất ra HTML trên trang. Điều này có thể được thực hiện bằng thành phần kỳ diệu được gọi là `React.Fragment`, và nó có thể được sử dụng như loại phần tử nhóm. Hãy làm điều đó trong đoạn mã sau.




const title = React.createElement("h1", null, "Hello world!");
const link = React.createElement("a", { href: "//react.dev" }, "Read more");
const group = React.createElement(
    React.Fragment, null, title, link
);
const domElement = document.getElementById("root");
ReactDOM.createRoot(domElement).render(group);

Repository: rq02-siblings-fragment
$ npx create-react-app rq02-siblings-frag --template rq02-siblings-fragment
https://rq2e.com/rq02-siblings-fragment

Kết quả của đoạn mã này được hiển thị trong hình 2.11 trên trình duyệt.
Bạn cũng có thể render toàn bộ phần tử trong một câu lệnh duy nhất như sau:

Figure 2.11 Title and link without a grouping element
 

Điều này chức năng tương đương với mã trước đó; nó chỉ sử dụng ít biến hơn. Một số người có thể cho rằng nó trở nên rõ ràng hơn, trong khi người khác có thể nói rằng nó trở nên ít đọc hơn.
Cho đến nay, bạn chủ yếu đã cung cấp các giá trị chuỗi như là tham số đầu tiên của `createElement()`. Nhưng tham số đầu tiên có thể có hai loại đầu vào, như chúng ta vừa thấy với các đoạn mã fragment:
- Thẻ HTML tiêu chuẩn dưới dạng chuỗi, ví dụ: "h1", "div" hoặc "p" (không có dấu ngoặc nhọn). Tên viết thường.
- Component React dưới dạng tham chiếu (không phải là chuỗi). Tên thường viết hoa.
Cách tiếp cận đầu tiên render các standard HTML elements. Bạn có thể sử dụng bất kỳ chuỗi nào làm tên thẻ HTML, không phụ thuộc vào việc nó có ý nghĩa trong trình duyệt theo mặc định hay không. Do đó, trong khi bạn thường sẽ sử dụng các phần tử HTML thông thường như `div`, `main`, `section`, và như vậy, nhưng không có điều gì ngăn bạn khỏi việc tạo một phần tử `tiny-horse`, nó sẽ được hiển thị là `<tiny-horse>` trong trình duyệt. Nó không có ý nghĩa và không có kiểu mặc định, nhưng nó vẫn hoạt động.



Trong cách tiếp cận thứ hai vừa liệt kê, chúng ta có thể cung cấp một Component React dưới dạng tham chiếu. Điều này không phải là tên của một Component React dưới dạng chuỗi, mà là một tham chiếu trực tiếp đến Component đó. Bạn đã thấy một ví dụ về điều này khi sử dụng `React.Fragment`. Bây giờ hãy xem cách chúng ta có thể tạo các Component tùy chỉnh của riêng mình trong phần tiếp theo.

2.4 Creating custom components

Sau khi nesting elements với React, bạn sẽ gặp vấn đề tiếp theo: có rất nhiều elements với nhiều sự lặp lại. Bạn cần sử dụng component based architecture (CBA) mà chúng tôi đã mô tả trong chương 1, cho phép bạn tái sử dụng mã bằng cách tách biệt separate functionality thành các phần không liên quan chặt chẽ: meet component classes, hoặc chỉ là các components, như chúng thường được gọi để ngắn gọn (không nên nhầm lẫn với các web components).

Hãy tưởng tượng các thẻ HTML tiêu chuẩn như các  building blocks. Bạn có thể sử dụng chúng để tạo ra các thành phần React của riêng bạn, mà bạn có thể sử dụng để tạo ra các phần tử tùy chỉnh (các instances của các components). Bằng cách sử dụng các custom elements, bạn có thể đóng gói encapsulate và trừu tượng hóa abstract logic trong các thành phần có thể sử dụng và tái sử dụng. Điều trừu tượng này cho phép các teams tái sử dụng giao diện người dùng (UI) trong các ứng dụng lớn, phức tạp cũng như trong các dự án khác nhau. Ví dụ bao gồm các panels, inputs, buttons, menus, và như vậy.

Trong ví dụ này, chúng ta muốn tạo ba links giống nhau. Việc tạo ra các links giống nhau không hoàn toàn có ý nghĩa, nhưng, tạm thời, chúng ta không thể tùy chỉnh chúng, vì vậy hãy chỉ làm theo tình huống này. Chúng ta muốn tạo ra ba links, tất cả đều nói " Read more about React " và link đến trang web React tại www.react.dev. Chúng ta cũng muốn bọc mỗi link trong một paragraph, để chúng xuất hiện trên các dòng riêng biệt.

Có hai cách tiếp cận khác nhau cho vấn đề này. Chúng ta có thể thực hiện cách làm ngây thơ bằng cách có ba bản sao đồng nhất của các elements, hoặc chúng ta có thể thực hiện cách thông minh bằng cách tạo một link component có thể tái sử dụng và sau đó khởi tạo nó ba lần, như minh họa trong hình 2.12. 
 

Hãy trước tiên xem xét cách tiếp cận đầu tiên, nơi chúng ta chỉ sử dụng một thành phần duy nhất với các bản sao được sao chép thủ công. Chúng ta muốn có ba links độc lập bên trong các paragraphs độc lập, và chúng ta có thể làm điều đó một cách khá dài dòng như trong đoạn mã sau.
const link1 = React.createElement(
    "a", { href: "//react.dev" }, "Read more about React");
const p1 = React.createElement("p", null, link1);
const link2 = React.createElement(
    "a", { href: "//react.dev" }, "Read more about React");
const p2 = React.createElement("p", null, link2);
const link3 = React.createElement(
    "a", { href: "//react.dev" }, "Read more about React");
const p3 = React.createElement("p", null, link3);
    
const group = React.createElement(React.Fragment, null, p1, p2, p3);
const domElement = document.getElementById("root");
ReactDOM.createRoot(domElement).render(group);

Nếu chúng ta mở nó trong trình duyệt, chúng ta sẽ có kết quả được hiển thị trong hình 2.13, đó chính xác là điều chúng ta muốn.
 
Nhưng chúng ta đang lặp lại nhiều lần trong đoạn mã 2.4, điều này, tất nhiên, không mong muốn. Toàn bộ ý nghĩa của React và các framework tương tự là ngăn chặn việc lặp lại chính bản thân chúng ta.

Điều này đòi hỏi một custom component!
Một custom component là một object có tên chứa các elements và các component instances khác. Vì vậy, trong trường hợp này, chúng ta có thể tạo một Link component duy nhất sẽ hiển thị liên kết theo cách chúng ta cần, và sau đó chúng ta sẽ bao gồm ba instance của Link component thay vì các phần tử "nguyên thủy" <p> và <a> với tất cả các thuộc tính của chúng.

Bạn tạo một React component class bằng cách extending lớp React. Component với cú pháp ES6 
class CHILD extends PARENT. Hãy tạo một custom Link component class bằng cách sử dụng class class Link extends React.Component
Một điều bắt buộc bạn phải triển khai cho class mới này là phương thức render(). Phương thức này phải trả về một single root element được tạo bằng createElement(), được tạo từ một custom component class khác hoặc một thẻ HTML. Cả hai đều có thể có các phần tử lồng nhau nếu bạn muốn miễn là chỉ có một phần tử root.

Listing 2.5 Creating and rendering a React component class
//Defines a `React component` class with the capitalized name Link
class Link extends React.Component {
  // Creates a render() method as an expression (function returning a single element)
  render() {
    return React.createElement(
      "p",
      null,
      React.createElement(
        "a",
        { href: "//react.dev"},
        "Read more about React"
      )
    )
  }
}

const link1 = React.createElement(Link);
const link2 = React.createElement(Link);
const link3 = React.createElement(Link);

const group = React.createElement(React.Fragment, null, link1, link2, link3);

const domElement = document.getElementById("root");
ReactDOM.createRoot(domElement).render(group);

Repository: rq02-custom-links
npx create-react-app rq02-custom-links --template rq02-custom-links
https://rq2e.com/rq02-custom-links

Theo quy ước, tên của các biến chứa các thành phần React được viết hoa chữ cái đầu. Điều này không bắt buộc trong JavaScript thông thường. Bạn có thể sử dụng tên lớp viết thường someLink trong mã trước đó thay vì Link và nó vẫn hoạt động. Nhưng vì nó là bắt buộc cho JSX (chúng ta sẽ bàn về nó trong chương tiếp theo), chúng ta áp dụng quy ước này ở đây.
Tương tự như ReactDOM.createRoot().render(), phương thức render() trong một class
component chỉ có thể trả về một phần tử duy nhất. Nếu bạn cần trả về nhiều phần tử cùng cấp, hãy bao gồm chúng trong một thành phần container - hoặc là một phần tử HTML hoặc một đoạn mã React. Nếu chúng ta chạy mã này trong trình duyệt ngay bây giờ, chúng ta sẽ có chính xác HTML giống như trước đó (xem hình 2.13).
Mã mới này gọn gàng hơn nhiều. Sự lặp lại không cần thiết đã được loại bỏ, và chúng ta đã phân chia một phần của mã có thể được sử dụng lại bất cứ lúc nào. Đây là sức mạnh của khả năng tái sử dụng thành phần! Nó dẫn đến sự phát triển nhanh chóng hơn và ít lỗi hơn. Components cũng có properties, life cycle events, states, DOM events, and other features giúp bạn làm cho chúng trở nên tương tác và tự chứa; những chủ đề này sẽ được thảo luận trong các chương tiếp theo.

Ngay bây giờ, các liên kết đều giống nhau. Điều tuyệt vời có phải là bạn có thể thiết lập attributes của các phần tử và sửa đổi content và/hoặc hành vi của chúng một cách riêng lẻ không? Bạn có thể làm điều đó bằng thuộc tính, như chúng ta sẽ thảo luận tiếp theo.

2.5 Working with properties

Properties là một phần quan trọng của declarative style mà React sử dụng. Hãy nghĩ về các properties như là giá trị không thay đổi bên trong một element. Chúng cho phép các elements có những biến thể khác nhau nếu được sử dụng trong một view, như việc thay đổi URL của một link bằng cách truyền một giá trị mới cho một thuộc tính:
React.createElement("a", { href: "//react.dev" }, "React");

Một điều cần nhớ là các properties không thể thay đổi bên trong các thành phần của chúng. Một phần tử cha gán các thuộc tính cho các phần tử con khi chúng được tạo ra. Phần tử con không được phép sửa đổi các thuộc tính của mình. Ví dụ, bạn có thể truyền thuộc tính `PROPERTY_NAME` với giá trị `VALUE` cho một thành phần có kiểu `Link`, như sau:
React.createElement(Link, { PROPERTY_NAME: VALUE });
Các thuộc tính chặt chẽ tương đồng với các thuộc tính HTML (như được thể hiện với href trong liên kết ở đoạn mã ở đầu phần này). Điều này là một trong những mục đích của chúng, nhưng chúng cũng có một mục đích khác - bạn có thể sử dụng các thuộc tính của một phần tử trong mã của bạn như bạn muốn cho các mục sau:
- Để hiển thị các thuộc tính HTML tiêu chuẩn của một phần tử: href, title, style, class, v.v.
- Như các hướng dẫn tùy chỉnh cho các thành phần để làm cho chúng hiển thị một cách riêng lẻ.
Đối tượng properties có thể được truy cập bên trong một component bằng cách sử dụng `this.props`. Đây là một đối tượng bị đóng băng (immutable), từ đó bạn chỉ có thể đọc giá trị, không thể set chúng.

Frozen objects in JavaScript
Bên trong, React sử dụng `Object.freeze()`, một hàm tích hợp trong JavaScript để làm cho đối tượng `this.props` trở thành không thể thay đổi. Để kiểm tra xem một đối tượng có bị đóng băng không, bạn có thể sử dụng phương thức `Object.isFrozen()`. Ví dụ, bạn có thể xác định xem câu lệnh sau có trả về true không:
class Test extends React.Component {
  render() {
    console.log(Object.isFrozen(this.props))  // -> true
    return React.createElement("div")
  }
}

Chi tiết về điều này khá phức tạp, nhưng hiện tại, quan trọng là bạn không nên cố gắng chỉnh sửa hoặc thêm các thuộc tính bên trong một component. Điều này được thực hiện trong ngữ cảnh của thành phần cha parent context.

2.5.1 A single property

Bắt đầu với một ví dụ rất đơn giản. Chúng ta muốn tên của framework trong các links chúng ta đã tạo trước đó có thể được tùy chỉnh. Vì vậy, chúng ta có thể nói "Read more about React" trong một liên kết, "Read more about Vue" trong thứ hai, và "Read more about Angular" trong thứ ba, như được thể hiện trong hình 2.14.
Để làm điều này, chúng ta cần thực hiện hai bước:
1. Truyền một property vào các component instances của chúng ta.
2. Sử dụng property bên trong component.

Đầu tiên, chúng ta cần truyền một property mới vào các thể hiện của link. Thay vì chỉ sử dụng
const link1 = React.createElement(Link);
chúng ta sẽ thay vào đó cung cấp một object làm đối số thứ hai với một thuộc tính duy nhất:
const link1 = React.createElement(Link, { framework: "React" }); 
Chúng ta đã sử dụng tên biến framework ở đây. Đó chỉ là một sự chọn lựa tùy ý mà chúng ta có thể thực hiện như là người tạo thành phần. Chúng ta chỉ cần đảm bảo sử dụng cùng tên biến trong bước thứ hai. Chúng ta bây giờ cần sử dụng propertyđã được truyền này bên trong class của chúng ta. Với giả định rằng chúng ta gọi biến này là framework, chúng ta sẽ truy cập nó thông qua `this.props.framework`. Đoạn mã toàn bộ kết quả được hiển thị trong đoạn mã dưới đây.
class Link extends React.Component {
  render() {
    console.log(this.props)
    return React.createElement(
      "p",
      null,
      React.createElement(
        "a",
        { href: "//react.dev" },
        `Read more about ${this.props.framework}`
      )
    )
  }
}

const link1 = React.createElement(Link, {framework: "React"});
const link2 = React.createElement(Link, {framework: "Vue"});
const link3 = React.createElement(Link, {framework: "Angular"});

const group = React.createElement(React.Fragment, null, link1, link2, link3);

const domElement = document.getElementById("root");
ReactDOM.createRoot(domElement).render(group);

2.5.2 Multiple properties

Có thể bạn đã nhận thấy rằng tất cả các link vẫn trỏ đến cùng một URL, đó là trang web của React. Điều đó không tốt, tất nhiên, vì chúng ta cần các URL khác nhau. Sử dụng cùng một phương pháp, chúng ta đơn giản là phát minh một thuộc tính mới, url, và sử dụng nó bên trong thành phần cũng như trong các thể hiện của thành phần. Bạn có thể thấy điều đó được minh họa trong biểu đồ trong hình 2.16 và được thực hiện trong mã trong danh sách 2.7.

 
Listing 2.7 Link instances with different text and URLs
class Link extends React.Component {
  render() {
    const link = React.createElement(
      "a",
      {href : this.props.url},
      `Read more about ${this.props.framework}`
    );
    return React.createElement('p', null, link);
  }
}

const link1 = React.createElement(Link, {
  framework: "React",
  url: "//react.dev"
});
const link2 = React.createElement(Link, {
  framework: "Vue",
  url: "//vuejs.org"
});
const link3 = React.createElement(Link, {
  framework: "Angular",
  url: "//angular.io"
});

const group = React.createElement(React.Fragment, null, link1, link2, link3);

const domElement = document.getElementById("root")
ReactDOM.createRoot(domElement).render(group);

Repository: rq02-link-props
$ npx create-react-app rq02-link-props --template rq02-link-props
https://rq2e.com/rq02-link-props
Bạn có thể thấy điều này được thực hiện trong trình duyệt trong hình 2.17. Như bạn thấy, chúng ta có thể sử dụng properties trên cả các custom components (được sử dụng bên trong thành phần để tùy chỉnh cấu trúc trả về) và các phần tử HTML (đặt các thuộc tính HTML).
 

Nhưng nếu bạn làm lộn và đặt một thuộc tính tùy chỉnh trên một phần tử HTML thì sao? React vẫn sẽ hiển thị nó. Trước React 16, các thuộc tính không hợp lệ sẽ được loại bỏ, nhưng vì ứng dụng web hiện đại thường sử dụng các thư viện bên thứ ba khác có thể phụ thuộc vào một số thuộc tính tùy chỉnh, nên React 16 và phiên bản sau đó sẽ cho phép bạn sử dụng bất kỳ thuộc tính nào bạn chọn.
Bạn có thể hoàn toàn thay đổi các elements được render dựa trên giá trị của một thuộc tính. Ví dụ, chúng ta có thể xem xét thuộc tính framework và trả về một tiêu đề lớn kèm theo liên kết nếu tên framework là "React":

class Link extends React.Component {
  render() {
    const link = React.createElement(
      "a",
      {href : this.props.url},
      `Read more about ${this.props.framework}`
    );
    if(this.props.framework === "React") {
      return React.createElement('h1', null, link)
    }
    return React.createElement('p', null, link);
  }
}

Điều này cũng là một ví dụ tuyệt vời về việc các React element chỉ là JavaScript thông thường. Chúng ta có thể tạo một element và lưu trữ nó trong một biến, sau đó sau này sử dụng biến đó như chúng ta muốn. Chúng ta cũng có thể tạo nhánh bằng cách sử dụng JavaScript functionality thông thường. Nếu chúng ta hiển thị component mới này trong trình duyệt, đột nhiên các link tags không còn giống nhau nữa, như bạn có thể thấy trong hình 2.18.
 
Bây giờ chúng ta đã bao quát nhiều biến thể của một số HTML rất đơn giản mà một mình gần như vô ích. Nhưng bằng cách bắt đầu nhỏ, chúng ta đang xây dựng một nền tảng vững chắc cho các chủ đề tiên tiến hơn trong tương lai. Sự thật là bạn có thể đạt được rất nhiều điều tuyệt vời với các custom component.
Việc hiểu cách React hoạt động trong JavaScript thông thường rất quan trọng nếu bạn (như nhiều nhà phát triển React khác) dự định sử dụng JSX. Điều này bởi vì cuối cùng, trình duyệt vẫn sẽ chạy JavaScript thông thường, và bạn sẽ cần hiểu kết quả của quá trình chuyển đổi từ JSX sang JS từ thời gian này sang thời gian khác. Tiếp theo, chúng ta sẽ sử dụng JSX, điều này sẽ được đề cập trong chương tiếp theo. Nhưng trước khi đi đến đó, chúng ta cần thảo luận một chút về cấu trúc của một ứng dụng React.
2.5.3 The special property: children

Các React elements có một thuộc tính đặc biệt, đó là children. Đây không phải là một thuộc tính bạn chỉ định theo cách thông thường, nhưng bạn sử dụng nó như bất kỳ thuộc tính nào khác.
Hãy thay đổi ví dụ của chúng ta một chút và thay vào đó tạo một danh sách các liên kết nơi văn bản chỉ là tên framework mà không có văn bản "Read more about" trước nó, như được thể hiện trong hình 2.19.

 
Bây giờ hãy đi một bước xa hơn. Giả sử chúng ta muốn hiển thị tên framework cho React ở dạng in đậm. Chúng ta đã biết cách tạo một phần tử in đậm - chỉ cần bọc nó trong một phần tử như sau:
React.createElement("strong", null, "React");

Nhưng làm thế nào chúng ta sẽ truyền nó vào dưới dạng thuộc tính? Chúng ta có thể làm điều này bằng cách tạo node cho framework React như sau:
const boldReact = React.createElement("strong", null, "React"); [1]
const link1 = React.createElement(Link,{ 
   framework: boldReact, url: "//react.dev"  [2]
});

1.	Creates a React element in the variable named boldReact
2.	Passes that variable in as the property framework on the Link element

Tuy nhiên, điều đó hơi kỳ quặc. Bây giờ chúng ta đang tạo các elements, nhưng lại truyền chúng vào dưới dạng properties, điều này không phải là cách chúng ta thường làm. Nhưng nếu chúng ta có thể tạo một element và truyền nó vào dưới dạng child element thì sao?

Nhớ cách argument ba và các argument tiếp theo của React.createElement là các children element của element? Chúng ta chưa sử dụng điều đó cho các component tùy chỉnh, nhưng chúng ta có thể làm điều đó. Tất cả các node passed as children cho một custom element có thể được truy cập thông qua `this.props.children`. Thuộc tính đó có thể là một single node (nếu chỉ truyền một phần tử con) hoặc một mảng các nodes (nếu truyền nhiều phần tử con).

Vậy nên, hãy thay đổi thành phần gốc của chúng ta để chứa ba links, trong đó link text không được truyền dưới dạng property có tên là `framework`, mà thay vào đó là một child node. Đối với link đầu tiên, chúng ta vẫn muốn làm cho văn bản in đậm, như được hiển thị trong hình 2.20 và sau đó được thực hiện trong mã nguồn 2.8.

 

class Link extends React.Component {
  render() {
    return React.createElement(
      "p",
      null,
      React.createElement(
        'a',
        {href: this.props.url},
        this.props.children
      )
    );
  }
}

const boldReact = React.createElement("strong", null, "React");
const link1 = React.createElement(Link, {url : "//react.dev"}, boldReact);
const link2 = React.createElement(Link, {url : "//vuejs.org"}, "Vue")
const link3 = React.createElement(Link, {url: "//angular.io"}, "Angular");

const group = React.createElement(React.Fragment, null, link1, link2, link3);

const domElement = document.getElementById('root');
ReactDOM.createRoot(domElement).render(group);


Repository: rq02-links-children

$ npx create-react-app rq02-links-children --template rq02-links-children

https://rq2e.com/rq02-links-children

Nếu bạn chạy điều này trong trình duyệt, bạn sẽ nhận được đầu ra được hiển thị trong hình 2.21. Sự phân biệt giữa việc sử dụng một thuộc tính bình thường và thuộc tính children có vẻ không quan trọng ở điểm này, nhưng trong chương tiếp theo, khi chúng ta bắt đầu sử dụng JSX, bạn sẽ thấy cách nó trở nên có nghĩa khi được sử dụng đúng cách.

 


2.6 Application structure
Từ chương tiếp theo trở đi, chúng ta sẽ cấu trúc structure applications của mình theo cách tổ chức có tổ chức và mô hình tương tự để dễ nhận biết. Chúng ta cũng sẽ tuân theo cấu trúc tiêu chuẩn mà mẫu CRA mặc định cung cấp.

Trong các ví dụ trước đó trong chương này, chúng ta đặt application của mình trực tiếp vào tệp index.js trong thư mục source. Từ bây giờ, chúng ta sẽ sử dụng một App component tùy chỉnh như là root element của ứng dụng của chúng ta, và chúng ta sẽ render nó như là một đứa con duy nhất single child đến trình duyệt. Điều này có nghĩa là chúng ta sẽ không cần phải chạm vào src/index.js nữa. Nó sẽ giữ nguyên tệp giống như nó là cho tất cả các ứng dụng tương lai sử dụng CRA.

Để đạt được mục đích này, chúng ta sẽ viết lại ứng dụng của mình với ba links trước đó thành hai new components. Một là ứng dụng root App và cái kia là Link component. Chúng ta sẽ sử dụng component Link này ba lần trong App component. Cuối cùng, chúng ta sẽ giải cấu trúc một số properties từ không gian tên React để rút gọn định nghĩa thành phần của mình một chút. Chúng ta sẽ đặt tất cả điều này trong src/App.js. Xem hình 2.22 và mã nguồn 2.9.
 

Listing 2.9 Application that goes in src/App.js

import React, {Fragment, Component, createElement} from "react";
class Link extends Component {
  render() {
    return createElement(
      "a",
      { href : this.props.url},
      `Read more about ${this.props.framework}`
    )
  }
}

class App extends Component {
  render() {
    const link1 = createElement(Link, {
      framework: "React",
      url: "//react.dev"
    });
    const link2 = createElement(Link, {
      framework: "Vue",
      url: "//vuejs.org"
    });
    const link3 = createElement(Link, {
      framework: "Angular",
      url: "//angular.io"
    });
    return createElement(Fragment, link1, link2, link3);
  }
}

export default App;




Chúng ta sau đó sẽ thay đổi src/index.js để import App từ App.js và render nó vào root DOM element, như được hiển thị trong mã nguồn 2.10.

Listing 2.10 src/index.js

import React from "react";
import {createRoot} from "react-dom/client";
import App from "./App";
createRoot(document.getElementById('root')).render(App);

File src/index.js mới này giờ đã hoàn chỉnh. Chúng ta không cần phải chỉnh sửa nó bao giờ nữa; chúng ta chỉ cần chỉnh sửa src/App.js để tùy chỉnh ứng dụng trong tương lai của mình.

Repository: rq02-links-app
$ npx create-react-app rq02-links-app --template rq02-links-app
https://rq2e.com/rq02-links-app

Khi ứng dụng của chúng ta lớn lên, chúng ta sẽ cần nhiều hơn là chỉ đặt mọi thứ trong một file duy nhất trong src/App.js. Khi cần phải mở rộng, chúng ta chỉ cần tạo các file mới và import chúng khi cần thiết. Mặc dù thường quy ước tạo một file duy nhất cho mỗi component và đặt tên tệp theo component đó (bao gồm cả chữ cái đầu tiên viết hoa), nhưng đó không phải là một quy tắc nghiêm ngặt. Nếu một component cần một số thành phần nhỏ khác để hoạt động, bạn có thể tự do quyết định liệu bạn muốn đặt tất cả trong một tệp, như chúng ta đã làm với Link và App trong listing 2.10, hoặc chia nó thành nhiều tệp.

Hãy xem cách chúng ta sẽ tạo ví dụ tương tự với các component App và Link trong các tệp riêng biệt. Vui lòng tham khảo sơ đồ trong hình 2.23. Chúng ta cũng sẽ cần cập nhật src/App.js để import component Link từ src/Link.js, như được hiển thị trong listing 2.11.

 

Listing 2.11 One component per file: src/App.js

import React, {Fragment, Component, createElement} from "react";
import Link from "./Link"

class App extends Component {
  render() {
    const link1 = createElement(Link, {
      framework: "React",
      url: "//react.dev"
    });
    const link2 = createElement(Link, {
      framework: "Vue",
      url: "//vuejs.org"
    });
    const link3 = createElement(Link, {
      framework: "Angular",
      url: "//angular.io"
    });
    return createElement(Fragment, link1, link2, link3);
  }
}

export default App;

Sau đó, chúng ta phải tạo ra tệp src/Link.js mới chỉ chứa Link component và nhớ export nó ở cuối.
Listing 2.12 One component per file: src/Link.js

import React from "react";

class Link extends React.Component {
    render() {
        return React.createElement('p', null,
            React.createElement(
                "a",
                { href: this.props.url },
                `Read more about ${this.props.framework}`
            )
        );
    }
}

export default Link;

Repository: rq02-links-app-alt
$ npx create-react-app rq02-links-app-alt --template rq02-links-app-alt
https://rq2e.com/rq02-links-app-alt

Chúng ta sẽ sử dụng cả hai phương pháp trong suốt cuốn sách. Trong nhiều chương sắp tới, ứng dụng của chúng ta sẽ nhỏ gọn và đầy đủ, nên chúng ta sẽ đặt mọi thứ bên trong src/App.js. Nhưng ở các chương sau, ứng dụng của chúng ta sẽ ngày càng lớn hơn và chúng ta sẽ phải vượt qua một tệp duy nhất. Chúng ta cũng sẽ tạo ra các tệp cho những thứ khác ngoài components. Đó có thể là các tệp cho các functions thường được sử dụng hoặc các shared functionality khác mà chúng ta muốn sử dụng trong nhiều tệp. Chúng ta cũng sẽ sử dụng các tệp riêng lẻ cho các custom hooks khi chúng ta đến chủ đề đó trong chương 10.

Khi dự án trở nên lớn hơn, cấu trúc thư mục được giới thiệu. Không có tiêu chuẩn xác định về cách sử dụng thư mục để cấu trúc một dự án React, nên các nhóm thường xuyên đưa ra những quy tắc tốt nhất của riêng họ.


2.7 Quiz

1 A custom React component can be created with which of the following
statements?
a const Name = React.createComponent()
b class Name extends React.Component
c const Name = React.createElement()
d class Name extends React.Class

2 The only mandatory member of a React component is which of the following?
a function
b return
c name
d render
e class

3 To access the url property inside a component, you use which of the following?
a this.properties.url
b this.data.url
c this.props.url
d url

4 React properties are immutable inside the component itself. True or false?
5 React components allow developers to create reusable UIs. True or false?

Quiz answers

Dịch:

1. class Name extends React.Component. Không có `React.Class` hoặc `React.createComponent`, và `React.createElement` được sử dụng để tạo các thể hiện của các thành phần, không phải định nghĩa chúng.

2. render() là bắt buộc. Các từ khóa `function`, `return`, và `class` không phải là tên phương thức hợp lệ.

3. this.props.url là chính xác, bởi vì chỉ có `this.props` trả về properties
object.

4. True. Không thể thay đổi một property bên trong component itself.

5. True. Nhà phát triển sử dụng các thành phần để tạo giao diện người dùng có thể tái sử dụng.

Summary

 Bạn có thể tạo React projects mới bằng cách sử dụng command-line program 
createreact-app. Điều này giúp bạn nhanh chóng bắt đầu với một bộ khởi đầu tốt với các thư viện quý giá.
  
 New React projects có thể được tạo từ một template cụ thể, và tất cả các ví dụ trong cuốn sách này đều đi kèm với một template để cho bạn xem ví dụ đó một cách nhanh chóng chỉ trong ba lệnh mà không cần tìm kiếm hoặc tải xuống bất cứ thứ gì trực tiếp. Chúng tôi cũng sẽ cung cấp links để tải xuống các ví dụ nếu cần.
  
 Bạn có thể lồng nest các React elements bằng cách đặt các cuộc gọi createElement() lồng nhau vào bên trong nhau. Bạn có thể tạo ra các nút anh em sibling nodes bằng cách sử dụng các đối số thứ ba, thứ tư, và cứ như vậy trong createElement().
  
 Bạn có thể tạo các elements dựa trên tên HTML node thông thường bằng cách sử dụng tên nút HTML làm đối số đầu tiên cho createElement().
  
 Nếu bạn muốn sửa đổi các elements kết quả bằng cách sử dụng properties, bạn có thể truyền chúng vào dưới dạng đối tượng như là đối số thứ hai cho createElement().
  
 Để sử dụng CBA (một trong những tính năng của React), bạn tạo các custom components. Các Custom components có thể sử dụng thuộc tính nội tại properties internally thông qua biến this.props. Các child nodes được nhận bằng property đặc biệt có tên là children.
  
 Các ví dụ trong cuốn sách này sẽ tuân theo một cấu trúc tệp rất đơn giản.

Chapter 3 - Introduction to JSX
This chapter covers
 Understanding JSX and its benefits
 Using JSX to implement custom components faster and easier
 React and JSX gotchas
JavaScript XML (JSX) là một phần mở rộng cú pháp cho JavaScript. Điều này làm cho React trở nên xuất sắc, nhưng cũng là một trong những yếu tố gây tranh cãi khi React được giới thiệu vào ngày xưa.
Dưới đây là một ví dụ về việc sử dụng JSX trong JavaScript:
const link = <a href="//react.dev">React</a>;
JSX là phần tử xuất hiện giữa dấu ngoặc nhọn: `<a href="//react.dev">React</a>`. Nó không phải là một chuỗi, không phải là một biểu thức mẫu, và không phải là HTML. Đó là một đối tượng JavaScript được tạo ra bằng cú pháp mở rộng gọi là JSX. Nó giúp tạo ra các phần tử React nhanh hơn và gọn gàng hơn, cũng như làm cho việc đọc các React elements trở nên dễ dàng hơn. Ưu điểm sau cùng ít nhất cũng quan trọng như ưu điểm trước.
JSX chỉ dành cho các nhà phát triển. Một mình nó không làm gì cả để cải thiện hoặc tăng tốc ứng dụng web. JSX được chuyển đổi thành mã code giống như khi không sử dụng JSX.

Mặc dù JSX không phải là một yêu cầu, nhưng nó được chấp nhận phổ biến như là cách duy nhất để viết các React component. Bạn có thể thấy một số team không sử dụng JSX, nhưng chúng chiếm một phần nhỏ rất lớn.
Trong chương này, chúng ta sẽ đào sâu hơn vào những lí do sử dụng JSX ban đầu, sau đó thảo luận về tất cả các phần khác nhau của việc áp dụng JSX trong thực tế, và cuối cùng, đề cập đến một số mẹo mà bạn cần chú ý khi sử dụng JSX. Trong quá trình này, chúng ta cũng sẽ thảo luận ngắn gọn về việc chuyển đổi JSX thành JavaScript, gọi là transpiling, mà bạn có thể nhớ từ chương 2. May mắn thay, transpiling không phải là điều bạn cần lo lắng quá nhiều.
LƯU Ý: Mã nguồn cho các ví dụ trong chương này có sẵn tại https://rq2e.com/ch03. Nhưng như bạn đã học ở chương 2, bạn có thể khởi tạo tất cả các ví dụ trực tiếp từ dòng lệnh bằng một lệnh duy nhất.
3.1 Why do we use JSX?

JSX là JavaScript extension cung cấp syntactic sugar (tức là làm cho việc nhập liệu dễ dàng hơn, nhưng về cơ bản là tương đương chức năng) cho việc gọi hàm function calls và object construction, đặc biệt là thay thế cho React.createElement(). Nó có thể trông giống một template engine hoặc HTML, nhưng thực tế không phải như vậy. JSX tạo ra các React elements trong khi vẫn cho phép bạn tận dụng toàn bộ sức mạnh của JavaScript. JSX là một cách tuyệt vời để viết các React component và bao gồm những lợi ích sau:

1. Trải nghiệm phát triển tốt hơn —  Mã nguồn dễ đọc hơn vì nó trở nên duyên dáng hơn, nhờ vào cú pháp giống XML giúp biểu diễn cấu trúc kêu gọi lồng nhau một cách tốt hơn.

2. Thông báo lỗi tốt hơn — React giả định rằng bạn sử dụng JSX và báo cáo các thông báo lỗi hữu ích như bạn thực sự sử dụng nó. Nếu không, thông báo lỗi sẽ hơi đưa lạc, đề cập đến một cú pháp khác mà bạn không sử dụng.

3. Faster code — Khi chuyển đổi JSX thành JavaScript, trình biên dịch tối ưu hóa mã nguồn ngay lập tức, làm cho JavaScript kết quả chạy nhanh hơn so với việc bạn nhập liệu bằng tay.

4. Thành viên nhóm làm việc hiệu quả hơn — Những nhà phát triển không chuyên nghiệp (ví dụ: nhà thiết kế) có thể dễ dàng sửa đổi mã nguồn vì JSX trông giống như HTML, mà họ đã quen thuộc.

5. Ít lỗi cú pháp hơn — Những nhà phát triển phải gõ ít mã hơn, điều này có nghĩa là họ mắc ít lỗi hơn.

Mặc dù JSX không bắt buộc cho React, nhưng nó tích hợp một cách tốt và chúng ta khuyến khích sử dụng nó, như cũng được khuyến nghị bởi những người sáng tạo React. Bạn sẽ gặp khó khăn để tìm thấy bất kỳ nhóm nào trong thế giới thực sự sử dụng React mà không sử dụng JSX. Mặc dù chúng ta không thể khẳng định rằng tất cả các dự án React gần đây trên thế giới đều sử dụng JSX, nhưng chúng ta rất tự tin rằng hầu hết họ đều sử dụng nó.
3.1.1 Before and after JSX

Để minh họa sự duyên dáng của JSX, dưới đây là đoạn mã snippet để tạo một element với một số custom components , sau đó là một link:
const element = <main>
<Title>Welcome</Title>
<Carousel images={6} />
<a href="/blog">Go to the blog</a>
</main>;
Đoạn mã trên là hoàn toàn giống với đoạn mã dưới đây được triển khai mà không sử dụng JSX:

const element = React.createElement(
  'main',
  null,
  React.createElement(Title, null, 'Welcome'),
  React.createElement(Carousel, {images: 6}),
  React.createElement('a', {href: "/blog"}, 'Go to the blog'),
);
Chúng ta có thể đồng thuận rằng phiên bản JSX dễ hiểu hơn rất nhiều khi nhìn nhanh. Nó giống như HTML, rất dễ đọc, và một phần giống với đầu ra HTML sẽ được hiển thị, ngoại trừ các thành phần tùy chỉnh, tất nhiên.
3.1.2 Keeping HTML and JavaScript together
Đơn giản mà nói, JSX là một ngôn ngữ nhỏ small language với cú pháp giống XML. Nó đã thay đổi cách mọi người viết các (UI) components. Trước đây, các nhà phát triển viết HTML và mã JavaScript cho controllers và views theo kiểu MVC, nhảy giữa các tệp khác nhau. Điều này xuất phát từ ngày đầu tiên của việc phát triển web. Phương pháp này phục vụ web tốt khi nó chỉ bao gồm HTML tĩnh, một ít CSS và một chút JavaScript để làm cho văn bản nhấp nháy.
Tuy nhiên, hiện nay chúng ta xây dựng UI tương tác cao, và JavaScript và HTML liên kết chặt chẽ để triển khai các chức năng khác nhau. Điều này vi phạm nguyên tắc về việc tách biệt các loại concerns (separation of concerns), nguyên tắc cơ bản trong hầu hết software development. Nguyên tắc principle này là về việc tách biệt các mục không liên quan, nhưng giữ các mục liên quan lại với nhau. Nếu bạn muốn tuân theo nguyên tắc này, bạn nên phân chia mã của mình break your code down sao cho mỗi bit trong sự cô lập thực hiện một và chỉ một concern, và những "bits" này sau đó có thể được sử dụng trong các kết nối khác nhau different connections. Nếu split your template và your view logic, nhưng chúng chỉ hoạt động nếu kết hợp lại, thì bạn đã tách một cách không cần thiết hai mục liên quan đến nhau.

React khắc phục vấn đề này bằng cách tổng hợp UI description và logic JavaScript; và với JSX, mã nguồn trông giống như HTML và dễ đọc và viết hơn. Nếu không có lý do gì khác, chúng ta sẽ sử dụng React và JSX cho cách tiếp cận mới này trong việc viết UI.

JSX được biên dịch bởi các công cụ chuyển đổi khác nhau thành ECMAScript chuẩn (xem hình 3.1). Có thể bạn biết rằng JavaScript cũng là ECMAScript, nhưng JSX không phải là một phần của quy định và không có bất kỳ ngữ nghĩa cụ thể nào. Điều này có nghĩa là nếu bạn cố gắng biên dịch JavaScript với JSX nhúng trong một trình biên dịch JavaScript thông thường mà không biên dịch JSX trước, bạn sẽ gặp lỗi. JSX không phải là JavaScript hợp lệ một mình và không thể được biên dịch trực tiếp bởi trình biên dịch JavaScript.

LƯU Ý: Chúng tôi gọi nó là biên dịch thay vì biên soạn vì chúng tôi chuyển đổi nó từ một ngôn ngữ nguồn (JSX) sang một ngôn ngữ nguồn khác (JavaScript). JavaScript kết quả sau đó, lần lượt, sẽ được thông dịch bởi một trình biên dịch "thực sự" chạy mã. Việc biên dịch chỉ là chuyển đổi cú pháp thay vì thông dịch mã.

Khi trình duyệt của bạn thực thi ứng dụng React của bạn, trình duyệt của bạn sẽ chỉ nhìn thấy các câu lệnh React.createElement cần thiết để tạo ra cấu trúc mà bạn cần. Chỉ có trong trình soạn thảo mà JSX tồn tại. Trình biên dịch chuyển đổi các tệp của bạn chứa JSX thành JavaScript thuần với các React.createElement() rải rác khắp nơi để giúp bạn tiết kiệm công sức.

Bạn có thể tự hỏi tại sao bạn nên bận tâm với JSX chút. Xem xét cách mã JSX trông ban đầu đối với những nhà phát triển mới, không ngạc nhiên khi một số nhà phát triển bị tắt hứng thú bởi công nghệ tuyệt vời này. Ví dụ, đoạn mã JavaScript sau có JSX giữa đó, kết hợp các dấu ngoặc nhọn ở nơi mà chúng thường không xuất hiện:
const title = <h1>Hello</h1>;
Nhưng điều làm cho JSX tuyệt vời là các phím tắt đến React.createElement(NAME, ...). Thay vì viết lại cuộc gọi hàm đó nhiều lần, bạn có thể sử dụng <NAME />. Và như đã đề cập trước đó, bạn càng gõ ít, càng ít lỗi bạn mắc phải. Với JSX, trải nghiệm của nhà phát triển là mối quan tâm chính, tức là làm cho việc tạo ra các thành phần và ứng dụng nhanh chóng hơn và ít lỗi hơn.
Lý do chính để sử dụng JSX là nhiều người thấy rằng mã có dấu ngoặc nhọn (<>), dễ đọc hơn so với mã chứa nhiều câu lệnh React.createElement(). Khi bạn đã quen với việc nghĩ về <NAME /> không phải là XML mà là một định danh cho mã JavaScript, bạn sẽ vượt qua sự lạ lẫm ban đầu của cú pháp JSX. Biết và sử dụng JSX có thể tạo ra sự khác biệt lớn khi bạn phát triển các React component và sau đó là các ứng dụng sử dụng React.

Như đã đề cập trước đó, JSX cần được biên dịch thành JavaScript thông thường trước khi trình duyệt có thể thực thi mã. Trong hầu hết các cài đặt, bạn sẽ không cần lo lắng về điều này, nhưng chúng ta sẽ thảo luận về một số công cụ biên dịch trong phần 3.3 nếu bạn cần tự thực hiện nó. Bây giờ, hãy đào sâu để hiểu rõ hơn về JSX.
3.2 Understanding JSX

Hãy khám phá cách làm việc với JSX. Bạn có thể đọc phần này và lưu nó vào đánh dấu cho tài liệu tham khảo của bạn, hoặc (nếu bạn muốn chạy một số ví dụ mã trên máy tính của mình) bắt đầu làm việc với các ví dụ sử dụng các mẫu create-react-app (CRA) được liệt kê ở khắp mọi nơi. Với CRA, bạn có JSX được biên dịch "miễn phí," nghĩa là bạn không cần lo lắng về việc tự thiết lập nó.

3.2.1 Creating elements with JSX
Tạo các React elements bằng JSX rất đơn giản. Hãy xem bảng 3.1 để xem một số ví dụ về mã JavaScript mà bạn đã sử dụng trước đó và phiên bản tương đương của nó trong JSX.

 

Trong mã JSX, các thuộc tính và giá trị của chúng (ví dụ, size={6}) xuất phát từ đối số thứ hai của hàm createElement(). Chúng ta sẽ tập trung vào làm việc với các thuộc tính sau trong chương sau.
Hiện tại, hãy xem một ví dụ về các JSX elements without properties. Dưới đây là một ví dụ từ chương trước được nâng cấp sang cấu trúc được khuyến khích recommended structure bằng cách sử dụng một App component tùy chỉnh. Nó chỉ là một phần tử h1 với văn bản "Hello world!", trong đó từ "world" được đặt chếch, như thể hiện dưới đây.

Listing 3.2 Emphasized greeting with JSX

import React, { Component } from 'react';
class App extends Component {
   render() {
     return <h1>Hello <em>World</em>!</h1>;
   }
}
export default App;


Bạn có thể thậm chí lưu trữ các objects được tạo với JSX syntax trong các biến vì JSX chỉ là một cải tiến cú pháp của React.createElement(). Ví dụ này lưu trữ tham chiếu đến element được tạo ra trong một biến trước khi trả về nó:
const title = <h1>Hello <em>World</em>!</h1>;
return title;
Điều này hoàn toàn giống với dòng 4 trong đoạn mã 3.2; nó chỉ sử dụng một biến phụ trước khi trả về.

3.2.2 Using JSX with custom components

Các ví dụ trước đã sử dụng thẻ JSX <h1>, đó cũng là tên thẻ HTML tiêu chuẩn. Khi làm việc với các component tùy chỉnh, bạn áp dụng cú pháp tương tự. Sự khác biệt duy nhất là component class name phải bắt đầu bằng một chữ cái viết hoa, như trong <Title />. Đoạn mã 3.3 cho thấy một phiên bản phức tạp hơn của ứng dụng ba links của chúng ta từ chương 2, được viết lại bằng JSX. Trong trường hợp này, bạn tạo một class component mới và sử dụng JSX để tạo một phần tử từ nó. Nhớ ví dụ Link của chương trước không? Đoạn mã trông như sau mà không có JSX (đã chuyển đổi sang cấu trúc App được khuyến nghị).
Listing 3.3 Three identical links without JSX
import React, { Component, Fragment } from 'react';
class Link extends Component {
    render() {
        return React.createElement(
            'p',
            null,
            React.createElement(
                'a',
                { href: '//react.dev' },
                'Read more about React',
            ),
        );
    }
}
class App extends Component {
    render() {
        const link1 = React.createElement(Link);
        const link2 = React.createElement(Link);
        const link3 = React.createElement(Link);
        const group = React.createElement(Fragment, null, link1, link2, link3);
        return group;
    }
}
export default App;

Sử dụng JSX, đoạn mã này trở thành Listing 3.4. Nếu bạn chạy nó trong trình duyệt, bạn sẽ nhận được kết quả giống như chúng ta đã thấy trong hình 2.13 ở chương 2, và chúng tôi hiển thị lại trong hình 3.2.

Listing 3.4 Three identical links with JSX
import React, { Component, Fragment } from "react";
class Link extends React.Component {
  render() {
    return (
      <p>
        <a href="//react.dev">Read more about React</a>
      </p>
    );
  }
}

class App extends React.Component {
  render() {
    return (
      <Fragment>
        <Link/>
        <Link/>
        <Link/>
      </Fragment>
    );
  }
}
export default App;

 

Repository: rq03-jsx-links
$ npx create-react-app rq03-jsx-links --template rq03-jsx-links
https://rq2e.com/rq03-jsx-links

3.2.3 Multiline JSX objects

Có thể bạn đã chú ý đến dấu ngoặc đơn quanh đối tượng JSX nhiều dòng multiline JSX được trả về trong listing 3.4. Bạn phải bao gồm những dấu ngoặc đơn này nếu bạn bắt đầu một đối tượng JSX nhiều dòng trên một dòng riêng sau một câu lệnh return, ví dụ, như sau. Đây là cách để tạo đối tượng JSX nhiều dòng khi không bắt đầu trên cùng một dòng:

```jsx
return (
  <main>
    <h1>Hello world</h1>
  </main>
);
```

Hoặc, bạn có thể bắt đầu root element của mình trên cùng một dòng với câu lệnh return và tránh sử dụng dấu ngoặc đơn. Ví dụ, điều này cũng là hợp lệ:

```jsx
return <main>
  <h1>Hello world</h1>
</main>;
```

Một nhược điểm của cách tiếp cận thứ hai này là giảm khả năng nhìn thấy thẻ mở <main>. Nó có thể dễ bị bỏ qua trong mã nguồn. Quyết định là ở bạn. Chúng tôi sẽ sử dụng phong cách trước đây của việc sử dụng dấu ngoặc đơn xung quanh nội dung JSX nhiều dòng để duy trì tính nhất quán. Lưu ý rằng điều tương tự cũng áp dụng cho bất kỳ việc sử dụng nào của đối tượng JSX nhiều dòng khác, ví dụ, khi bạn lưu chúng trong một biến. Chúng tôi cũng sẽ sử dụng dấu ngoặc đơn ở đó:

```jsx
const message = (
  <main>
    <h1>Hello world</h1>
  </main>
);
```
3.2.4 Outputting variables in JSX
Khi bạn xây dựng các components, bạn muốn chúng đủ thông minh để thay đổi giao diện dựa trên một số mã. Ví dụ, nếu một date component sử dụng ngày và giờ hiện tại, thay vì chỉ một giá trị được đặt cứng.
Khi làm việc với React chỉ bằng JavaScript, bạn phải sử dụng chuỗi template literals (tức là dấu backticks) để kết hợp chuỗi với biến - hoặc, tệ hơn, là nối chuỗi. Ví dụ, để sử dụng một biến trong ngữ cảnh chuỗi trong một thành phần DateTimeNow mà không có JSX, bạn sẽ viết mã như sau:

class DateTimeNow extends React.Component {
  render() {
    const dateTimenow = new Date().toLocaleString();
    return React.createElement(
      "span", 
      null,
      `Current date and time is ${dateTimenow}`
    )
  }
}

Trong JSX, bạn có thể sử dụng cú pháp ngoặc nhọn {} để đầu ra biến động, giảm độ phức tạp của mã đáng kể:

class DateTimeNowJSX extends React.Component {
  render() {
    const dateTimeNow = new Date().toLocaleString();
    return <span>Current date and time is {dateTimeNow}</span>
  }
}

Nếu bạn tham chiếu đến một biến là một phần tử React (tùy chọn được tạo bằng JSX), bạn có thể chèn trực tiếp phần JSX đó trong ngữ cảnh hiện tại:

const now = <date>{dateTimeNow}</date>
const message = <p>Tody is {now}</p>

Điều này tương đương với việc chèn trực tiếp phần tử:
const message = <p>Tody is <date>{dateTimeNow}</date></p>

Các biến được chèn cũng có thể là các thuộc tính, không chỉ là các biến được định nghĩa cục bộ:
<p>Hello {this.props.userName}, today is {dateTimeNow}.</p>
Bạn cũng có thể gọi các phương thức của component mà bạn tạo. Điều này là một thực hành phổ biến để cô lập các phần của chức năng isolate bits of functionality, như được thể hiện trong đoạn mã tiếp theo.
Listing 3.5 ButtonList using a method
class ButtonList extends Component {
  getButton(text) {
    return (
      <button disabled={this.props.disabled}>{text}</button>
    );
  }

  render() {
    return (
      <aside>
        {this.getButton("Up")}
        {this.getButton("Down")}
      </aside>
    );
  }
}

Ví dụ trong danh sách 3.5 được đơn giản hóa quá mức, tất nhiên, vì hầu hết thời gian, bạn có thể sử dụng một thành phần phụ  extra component cho một trường hợp sử dụng như vậy. Tuy nhiên, có những tình huống nơi các phương thức của thành phần thực sự hữu ích. Mục đích của ví dụ này là chỉ ra rằng bạn có thể gọi trực tiếp các phương thức của component trong JSX. Ví dụ, bạn có thể thực thi các biểu thức JavaScript tùy ý bên trong dấu ngoặc nhọn, như làm định dạng ngày trực tiếp:
<p>Today is {new Date(Date.now()).toLocaleTimeString()}.</p>
Bây giờ chúng ta hãy viết lại lời chào được nhấn mạnh của chúng ta để lưu trữ từ in nghiêng trong một biến trước khi xuất ra, trong đoạn mã tiếp theo. Sau đó, chúng ta sẽ tiếp tục thảo luận về cách bạn làm việc với các thuộc tính trong JSX ở phần tiếp theo.
Listing 3.6 Emphasized greeting using JSX and a variable
import { Component } from 'react';
class App extends Component {
  render() {
    const world = <em>World</em>;
    return <h1>Hello {world}!</h1>;
  }
}
export default App;

3.2.5 Working with properties in JSX

Chúng ta đã đề cập đến chủ đề này trước đó, khi giới thiệu về JSX. Element properties được định nghĩa bằng cú pháp attributes. Nói cách khác, bạn sử dụng cú pháp key1=value1 key2=value2… bên trong thẻ JSX để định nghĩa cả HTML attributes và React component properties. Điều này tương tự attribute syntax trong HTML/XML.
Nói một cách khác, nếu bạn cần truyền properties, hãy viết chúng trong JSX như bạn đã làm trong HTML thông thường. Bạn render standard HTML attributes bằng cách đặt các element properties (đã thảo luận trong phần 2.3) trên một React element với một thẻ HTML. Ví dụ, đoạn mã sau đặt một thuộc tính HTML tiêu chuẩn href cho phần tử mô phỏng `<a>`:
return <a href="/ /react.dev">Let's do React!</a>;

Bạn sử dụng cùng một phương pháp để setting property trên các custom component. Nếu chúng ta có Link component từ chương trước, chúng ta có thể sử dụng nó trong JSX như sau:
return <Link url="//react.dev" framework="React" />;

Việc sử dụng giá trị cứng cho thuộc tính không linh hoạt lắm, tất nhiên. Nếu bạn muốn tái sử dụng thành phần Link, thì href phải thay đổi để phản ánh một địa chỉ khác mỗi lần. Điều này được gọi là đặt giá trị động so với việc đặt cứng. Vì vậy, tiếp theo, chúng ta sẽ đi một bước xa hơn và xem xét một thành phần có thể sử dụng giá trị được tạo động cho thuộc tính. Những giá trị đó có thể đến từ các thuộc tính của thành phần (this.props). Sau đó, mọi thứ sẽ dễ dàng. Bạn chỉ cần sử dụng dấu ngoặc nhọn ({}) bên trong dấu ngoặc nhọn (<>) để truyền giá trị động của thuộc tính cho các phần tử.

Ví dụ, giả sử bạn đang xây dựng một component sẽ được sử dụng để liên kết đến tài khoản người dùng. Bạn cần một số thuộc tính trên thẻ `<a>`, nhưng href và title phải khác nhau cho mỗi component và không được đặt cứng. Hãy tạo một thành phần động ProfileLink mà render một liên kết với các thuộc tính url và label cho href và title, tương ứng. Bạn truyền các thuộc tính vào `<a>` bằng cách sử dụng {}:

class ProfileLink extends Component {
  render() {
    return (
      <a
        href={this.props.url} 
        title={this.props.label} 
        target="_blank">
      </a>
    );
  }
}

Giá trị của property đến từ đâu? Chúng được định nghĩa khi ProfileLink được tạo ra - tức là, trong component  tạo ra ProfileLink, còn được gọi là cha của nó. Ví dụ, đây là cách giá trị cho url và label được truyền khi một thể hiện ProfileLink được tạo ra, dẫn đến việc render thẻ `<a>` với những giá trị đó:

<ProfileLink url="/users/johnny" label="Profile for Johnny"/>

Từ chương trước, bạn sẽ nhớ rằng khi render các phần tử tiêu chuẩn (`<h>`, `<p>`, `<div>`, `<a>`, vv.), React sẽ render mọi thuộc tính ngay cả khi chúng không có bất kỳ ý nghĩa nghĩa nào trong HTML. Điều này không chỉ đối với JSX, đó chỉ là hành vi mặc định của React.
Nếu bạn có một object với các properties mà bạn muốn render trên một element, bạn có thể render từng cái một như sau:
return (
  <Post
    id={post.id}
    title={post.title}
    content={post.content}
  />
);
Điều này hoạt động tốt và là một giải pháp an toàn. Tuy nhiên, nếu bạn có một object với các values và bạn muốn render tất cả chúng, bạn có thể làm như vậy bằng cách sử dụng toán tử spread như sau:
return <Post {...post} />;
Lưu ý rằng điều này sẽ render tất cả các thuộc tính của đối tượng post, bất kể xem nó có ý nghĩa hay không. Chỉ sử dụng quy trình này khi bạn chắc chắn rằng đối tượng chỉ chứa các thuộc tính bạn cần hoặc ít nhất chắc chắn rằng bất kỳ thuộc tính dư thừa nào cũng bị bỏ qua. Điều này sẽ cho phép bạn cũng có thể render tất cả các properties được truyền vào một component cho một element khác bên trong thành phần đó bằng cách sử dụng toán tử spread:
return <input value={this.value} {...this.props} />;
Tuy nhiên, điều này có chút nguy hiểm, vì nó cho phép thành phần cha truyền vào các giá trị tùy ý có thể ghi đè lên bất kỳ giá trị nào bạn truyền vào nó. Nếu `this.props` chứa một thuộc tính giá trị, nó sẽ ghi đè lên thuộc tính giá trị mà bạn đã đặt trong thành phần trước khi sử dụng spread. Hãy cẩn thận khi sử dụng toán tử spread và đặc biệt là khi sử dụng spread cho tất cả các props được truyền vào một thành phần. Chúng ta sẽ quay lại với toán tử spread trong chương kế tiếp và bao quát một số ví dụ thường gặp khác về cách sử dụng nó.
THE SPECIAL PROPERTY: CHILDREN

Nếu bạn nhớ lại chương trước đó, chúng ta giới thiệu về thuộc tính đặc biệt `children`, mà chỉ giống như một thuộc tính bên trong một custom component, không nhìn thấy từ bên ngoài. Khi sử dụng JSX, thuộc tính `children` trở nên gọn gàng hơn để sử dụng. Trong ví dụ với các child nodes ở chương 2, nó trông giống như cấu trúc cây được hiển thị trong hình 3.3.

 
Hãy triển khai lại ví dụ này bằng JSX. Chúng ta biết tất cả những điều cần làm, vì vậy hãy tiến hành và thực hiện chúng.
import { Fragment, Component } from "react";

class Link extends Component {
  render() {
    return (
      <p>
        <a href={this.props.url}>
          {this.props.children}
        </a>
      </p>
    );
  }
}

class App extends Component {
  render() {
    return (
      <Fragment>
        <Link url="//react.dev">
          <strong>React</strong>
        </Link>
        <Link url="//vuejs.org">Vue</Link>
        <Link url="//angular.io">Angular</Link>
      </Fragment>
    );
  }
}

export default App;

Repository: rq03-children
$ npx create-react-app rq03-children --template rq03-children
https://rq2e.com/rq03-children
Sự khác biệt giữa việc sử dụng thuộc tính và nút con trở nên rõ ràng hơn nhiều. Chúng ta có thể đã truyền nội dung liên kết dưới dạng một thuộc tính, nhưng nó sẽ trông khá tệ. Nếu chúng ta sử dụng cách tiếp cận thuộc tính thông thường, nó sẽ trông như sau:
<Link
  url="//react.dev"
  content={<strong>React</strong>}
/>
Nhưng khi chúng ta sử dụng cách tiếp cận child node, nó trở thành:
<Link url="//react.dev">
  <strong>React</strong>
</Link>
Chắc chắn rằng chúng ta biết chúng ta ưa thích cách tiếp cận sau.
3.2.6 Branching in JSX

Branching nhánh luôn quan trọng trong lập trình. Ví dụ, nếu người dùng đã đăng nhập, hiển thị thông tin tài khoản của họ; ngược lại, hiển thị một form đăng nhập. Bởi vì JSX chỉ là JavaScript, chúng ta có thể sử dụng các cấu trúc hoàn toàn giống nhau như chúng ta thường làm trong lập trình thông thường regular coding để tạo rẽ nhánh create branching trong các component của chúng ta. Dù vậy, đã xuất hiện một số mô hình mà hầu hết các nhà phát triển tuân theo về cách sử dụng branching trong các React component sử dụng JSX:

- Sử dụng return sớm để rendering thị gì cả.
- Sử dụng toán tử ba ngôi để rendering các phần tử thay thế.
- Sử dụng toán tử AND logic (&&) để rendering các phần tử tùy chọn.
- Sử dụng object maps để rendering giữa nhiều elements khác nhau.
- Sử dụng các extra components cho các rẽ nhánh phức tạp hơn.
Chúng ta sẽ đi qua từng điều này trong các phần nhỏ tiếp theo để giải thích cách chúng ta sử dụng rẽ nhánh trong JSX và các custom React components của chúng ta.

USING EARLY RETURN FOR RENDERING NOTHING
Hãy tưởng tượng bạn có một component mà chỉ hiển thị nội dung liên quan khi một điều kiện cụ thể là đúng. 
Ví dụ, hãy tưởng tượng một component đếm ngược mà chỉ hiển thị giá trị khi số giây còn lại lớn hơn 0.
Nếu một thành phần không hiển thị gì cả, chúng ta có thể đơn giản là trả về `null` từ component. Tuy nhiên, để tối ưu hóa các component của chúng ta, chúng ta cố gắng thực hiện điều này càng sớm càng tốt để ngắn mạch thực hiện. Mục đích là chia nhánh ra thành trường hợp đơn giản nhất càng nhanh càng tốt để tránh thực hiện các tính toán thêm hoặc tạo các đối tượng JSX khi chúng ta không cần chúng.
Chúng ta có thể tạo Countdown component của mình như sau:
class Countdown extends Component {
  render() {
    const seconds = this.props.remaining % 60;
    const minutes = Math.floor(this.props.remaining / 60);
    const message = <p>{minutes}:{seconds}</p>;
    if (seconds > 0 || minutes > 0) {
      return message;
    } else {
      return null;
    }
  }
}
Không có gì inherently sai với cách tiếp cận này nó hoạt động và hoàn toàn chức năng. Nhưng bạn sẽ thấy nhiều nhà phát triển sử dụng cách tiếp cận của việc dừng sớm nếu component không hiển thị gì cả. Chúng ta có thể phát hiện trường hợp này của việc không hiển thị trước khi tính số giây và phút và trước khi tạo đối tượng JSX:

class Countdown extends Component {
  render() {
    if (this.props.remaining === 0) {
      return null;
    }
    const seconds = this.props.remaining % 60;
    const minutes = Math.floor(this.props.remaining / 60);
    return <p>{minutes}:{seconds}</p>;
  }
}
Ở đây, chúng ta cũng sử dụng việc khi chúng ta trả về từ bên trong một khối if, chúng ta không cần một khối else. Khối else là ngầm định trong việc rằng bất kỳ điều gì sau khối if chỉ được thăm nếu điều kiện thất bại.

USING TERNARY FOR LỰA CHỌN THAY THẾ ALTERNATIVES
Một trường hợp rất phổ biến trong các React components là hiển thị các elements khác nhau dựa trên regular if/else statement block. Ví dụ, hãy tưởng tượng một giỏ hàng trong đó chúng ta muốn hiển thị các mục nếu có bất kỳ mục nào, nhưng hiển thị một thông báo nếu không có mục nào trong giỏ hàng.
Chúng ta có thể thực hiện điều này trong JSX bằng cách sử dụng một biến và gán các giá trị khác nhau thông qua một khối câu lệnh if/else thông thường. Tuy nhiên, đây là một cách hơi dài dòng, và trong React, thì việc sử dụng toán tử ba ngôi là phổ biến hơn. Nơi mà câu lệnh if/else là một câu lệnh, toán tử ba ngôi là một biểu thức và có thể được sử dụng trực tiếp trong JSX như sau:
<p>User is {this.props.isOnline ? 'Online' : 'Offline'}</p>

Bằng cách sử dụng điều này, chúng ta có thể tạo shopping cart component của mình từ trước:

class ShoppingCart extends Component {
  render() {
    return (
      <aside>
        <h1>Shopping cart</h1>
        {this.props.items.length === 0 ? (
          <p>Your cart is empty. Go buy something!</p>
        ) : (
          <CartItems items={this.props.items} />
        )}
      </aside>
    );
  }
}
USING LOGICAL OPERATORS FOR OPTIONAL RENDERING
Một mô hình phổ biến khác là cần lựa chọn việc hiển thị một phần tử tùy thuộc vào điều kiện đúng, nhưng không hiển thị gì nếu điều kiện là sai. Ví dụ, chúng ta muốn hiển thị một biểu tượng đánh dấu (checkmark) bên cạnh tên người dùng nếu người dùng là người được xác minh, nhưng không hiển thị gì cho những người không được xác minh. Chúng ta có thể làm điều này bằng cách sử dụng toán tử logic AND và sự thật rằng các toán tử logic ngắn mạch (short-circuit) bằng cách trả về ngay sau khi sự đúng đắn của biểu thức toàn bộ được biết đến. Do đó, khi thực hiện a && b, JavaScript sẽ trả về a nếu a là giả định (falsy) hoặc b nếu a là đúng đắn (truthy). Nếu a là đúng đắn, không quan trọng b là gì; b sẽ được trả về bất kể. Kết hợp điều này với việc React hiển thị giá trị false như chuỗi rỗng (thêm về điều này sau).
Truthiness
Trong JavaScript, một giá trị truthy tương đương với true khi được đánh giá là Boolean. Ví dụ, trong một câu lệnh if:
if (someVariable) {
  // Điều này xảy ra nếu và chỉ nếu someVariable là truthy.
}
Giá trị là truthy nếu nó không phải là falsy. Đó là định nghĩa chính thức, không đùa. Chỉ có sáu giá trị falsy:
- false
- 0
- "" (chuỗi rỗng)
- null
- undefined
- NaN (không phải là số)
Chúng ta có thể sử dụng điều này để render các phần tử có điều kiện, bằng cách làm cho toán tử AND logic trả về false nếu người dùng không được xác minh và một phần tử React nếu người dùng đã được xác minh:


class UserName extends Component {
  render() {
    return (
      <p>
        {this.props.username}
        {this.props.isVerified && <Checkmark />}
      </p>
    );
  }
}
Bạn sẽ gặp mẫu này thường xuyên trong các React component, vì vậy đây là một điều cần biết
USING OBJECTS FOR SWITCHING
Cho đến nay, chúng ta đã xử lý trường hợp render một phần tử hoặc không render gì cả, hoặc render một phần tử hoặc phần tử khác, nhưng nếu chúng ta muốn render hơn hai loại phần tử dựa trên một điều kiện thì sao? Đối với tình huống này, chúng ta muốn render một icon dựa trên trạng thái của bài đăng blog. Nếu bài đăng ở trạng thái nháp, chúng ta sẽ render một biểu tượng nháp. Nếu bài đăng ở trạng thái đã xuất bản, chúng ta sẽ render một biểu tượng đã xuất bản. Và nếu bài đăng ở bất kỳ trạng thái khác nào (chúng ta đã biết đó chỉ là trạng thái đã xóa), chúng ta sẽ render một biểu tượng thùng rác.
Chúng ta có thể lồng các toán tử ba ngôi để kiểm tra trạng thái có phải là "draft" không; sau đó, nếu không phải, kiểm tra xem trạng thái có phải là "published" không; và nếu không phải, chúng ta giả định rằng nó phải đã bị xóa:
class PostStatus extends Component {
  render() {
    return this.props.status === "draft" ?
      <DraftIcon /> :
    this.props.status === "published" ?
      <PublishedIcon /> :
      <TrashIcon />;
  }
}
Điều này có thể hoạt động, nhưng không phải là cách làm đẹp. Một lựa chọn khác là sử dụng câu lệnh switch và đơn giản là trả về các giá trị khác nhau trong mỗi trường hợp. Tuy nhiên, một cách tiếp cận mô tả hơn ở đây là sử dụng một đối tượng với các thuộc tính cho các trường hợp khác nhau giải quyết các kết quả khác nhau:

const status2icon = {
  draft: <DraftIcon />,
  published: <PublishedIcon />,
  deleted: <TrashIcon />,
};
class PostStatus extends Component {
  render() {
    return status2icon[this.props.status];
  }
}
Đó là khá ngắn gọn và gọn gàng, phải không? Tuy nhiên, lưu ý rằng điều này không xử lý tình huống trong đó trạng thái không thuộc một trong những điều đó. Trước đây, component sẽ hiển thị biểu tượng trash nếu trạng thái không phải là draft hoặc published, nhưng bây giờ, nó chỉ sẽ hiển thị trash icon nếu trạng thái là deleted.

Để xử lý trường hợp khi trạng thái là bất kỳ giá trị không mong muốn nào khác, chúng ta cần thêm một phép toán OR logic ở cuối để nếu việc lập chỉ mục đối tượng không giải quyết gì cả, chúng ta vẫn hiển thị một giải pháp thay thế. Hãy nói chúng ta chỉ hiển thị biểu tượng rác trong mọi trường hợp không biết:
class PostStatus extends Component {
  render() {
    return status2icon[this.props.status] || status2icon.deleted;
  }
}
Mẫu này có lẽ ít phổ biến hơn trong React, nhưng bạn vẫn có thể thấy nó trong những trường hợp đơn giản như những trường hợp chúng ta đã thảo luận.
USING EXTRA COMPONENTS FOR COMPLEX BRANCHING
Các tình huống trước chỉ đề cập đến một số trường hợp chia nhánh đơn giản. Làm thế nào nếu component của bạn có logic phức tạp hơn? 
Hãy xem xét một ví dụ với một shopping cart component như trước đây với một số buttons ở phía dưới. Chúng ta phải triển khai business logic sau đây theo yêu cầu của khách hàng:
- Nếu người dùng đã đăng nhập, chỉ hiển thị nút Checkout.
- Nếu người dùng chưa đăng nhập, hiển thị nút Login cùng với nút Checkout as Guest.
- Nếu có bất kỳ sản phẩm nào hết hàng hoặc giỏ hàng trống, nút Checkout hoặc Checkout as Guest sẽ bị tắt.
- Nếu người dùng đã đăng nhập nhưng chưa thêm thẻ tín dụng, hiển thị nút Add Credit Card thay thế.
- Nếu người dùng đã đăng nhập, có thẻ tín dụng và đã nhập địa chỉ, hiển thị nút One-Click Buy kế bên nút Checkout. Nút này sẽ bị tắt theo cùng logic như nút Checkout.
Bây giờ, hãy triển khai tất cả điều này với những mẹo bạn đã học cho đến nay.

import { Component, Fragment } from "react";
class ShoppingCart extends Component {
  render() {
    const hasItems = this.props.items.length > 0;
    const isLoggedIn = this.props.user !== null;
    const hasCreditCard = isLoggedIn && this.props.user.creditcard !== null;
    const hasAddress = isLoggedIn && this.props.user.address !== null;
    const isAvailable = this.props.items.every((item) => !item.outOfStock);
    return isLoggedIn ? (
      hasCreditCard ? (
        <Fragment>
          <button disabled={!hasItems || !isAvailable}>
            Checkout
          </button>
          {hasAddress && (
            <button disabled={!hasItems || !isAvailable}>
              One-click buy
            </button>
          )}
        </Fragment>
      ) : (
        <button>Add credit card</button>
      )
    ) : (
      <Fragment>
        <button>Login</button>
        <button disabled={!hasItems || !isAvailable}>
          Checkout as guest
        </button>
      </Fragment>
    )
  }
}

class App extends Component {
  render() {
    const items = [1, 2, 3];
    const user = {creditcard: null, address: true};
    return <ShoppingCart items={items} user={user}></ShoppingCart>
  }
}

export default App;

Repository: rq03-cart-single
$ npx create-react-app rq03-cart-single --template rq03-cart-single
https://rq2e.com/rq03-cart-single

Được rồi, có vẻ như đã bao gồm mọi thứ. Tuy nhiên, điều này đang trở nên phức tạp với các điều kiện lồng nhau và thuộc tính lặp lại. Đối với trường hợp phức tạp như vậy, thường là một ý tưởng tốt để chia thành nhiều thành phần xử lý từng trường hợp khác nhau một cách riêng biệt.
Ở đây, chúng ta có thể tạo các components mới như <UserButtons /> và <GuestButtons />. Ở cấp độ cao nhất, chúng ta có thể chọn sử dụng components nào trong số chúng và sau đó thêm các điều kiện và điều kiện cần thiết bên trong từng components này.

Listing 3.9 Simplified multicomponent shopping cart
import { Component, Fragment } from "react";

class UserButtons extends Component {
  render() {
    const hasCreditCard = this.props.user.creditcard !== null;
    const hasAddress = this.props.user.address !== null;
    const disable = !this.props.canCheckout;
    return hasCreditCard ? (
      <Fragment>
        <button disabled={disable}>
          Checkout
        </button>
        {hasAddress && (
          <button disabled={disable}>One-click buy</button>
        )}
      </Fragment>
    ) : (
      <button>Add credit card</button>
    )
  }
}

class GuestButtons extends Component {
  render() {
    return (
      <Fragment>
        <button>Login</button>
        <button disabled={!this.props.canCheckout}>
          Checkout as guest
        </button>
      </Fragment>
    );
  }
}

class ShoppingCart extends Component {
  render() {
    const hasItems = this.props.items.length > 0;
    const isLoggedIn = this.props.users !== null;
    const isAvailable = this.props.items.every((item) => !item.outOfStock);
    const canCheckout = hasItems && isAvailable;
    return isLoggedIn ? (
      <UserButtons user={this.props.user} canCheckout={canCheckout}/>
    ) : (
      <GuestButtons canCheckout={canCheckout}/>
    )
  }
}

class App extends Component {
  render() {
    const items = [1, 2, 3];
    const user = {creditcard: null, address: true};
    return <ShoppingCart items={items} user={user}></ShoppingCart>
  }
}

export default App;

Repository: rq03-cart-multi
$ npx create-react-app rq03-cart-multi --template rq03-cart-multi
https://rq2e.com/rq03-cart-multi
Cách làm này hoạt động giống như trước đó với độ phức tạp hoàn toàn giống nhau, nhưng mỗi thành phần đơn giản hơn nhiều và bạn có thể dễ dàng hiểu từng thành phần khi đọc mã. Bạn thậm chí có thể tiến xa hơn bằng cách chia thành phần <User-Buttons> thành hai phần cho tình huống "có thẻ tín dụng" và "không có thẻ tín dụng".
Tất nhiên, chúng ta phải nhận thức rằng nhiều thành phần đồng nghĩa với nhiều mã nguồn, và nhiều mã nguồn có nghĩa là tăng cường bộ nhớ và sử dụng CPU hơn (nói chung). Do đó, ví dụ sau này này có chút chiếm tài nguyên hơn so với ví dụ trước. Tuy nhiên, trong hầu hết các ứng dụng, sự khác biệt này thường là không đáng kể, và chất lượng mã thường có ưu tiên hơn những tối ưu hóa nhỏ như vậy.
3.2.7 Comments in JSX
Vì JSX được viết bên trong JavaScript, bạn có thể sử dụng các comment thông thường của JavaScript bên ngoài các phần tử JSX như bình thường:
// This is the page title
const title = <h1>Hello world!</h1>;
Tuy nhiên, nếu bạn có đoạn mã JSX rất dài, bạn có thể muốn thêm comment bên trong JSX. Trong trường hợp đó, bạn không thể luôn sử dụng comment JavaScript thông thường trực tiếp.

Để thêm comment JSX giữa các thẻ, bạn có thể bọc comment JavaScript chuẩn bằng cặp {} với /**/ hoặc // như sau:
const content = (
  <div>
    {/* Just like a JS comment */}
    {/* It can also span
       multiple lines */}
    {// Single line comments are possible too
    }
  </div>
);
Bạn cũng có thể sử dụng comment JavaScript trực tiếp bằng cách sử dụng /**/ hoặc // bên trong thẻ:
const content = (
  <div>
    <input
      /* This element is
         rendered because... */
      name={this.props.name} // Some important comment here
    />
  </div>
);  
Lưu ý rằng khi bạn sử dụng comment thông thường trên một dòng giữa các thẻ bên trong dấu ngoặc nhọn, bạn cần có một ký tự xuống dòng trước khi kết thúc dấu ngoặc nhọn. Đoạn mã sau sẽ không hoạt động:



const content = (
  <div>
    {// This does NOT work! }
  </div>
);
Điều này sẽ dẫn đến một lỗi biên dịch vì dấu ngoặc nhọn kết thúc được coi là một phần của comment, nên dấu ngoặc nhọn mở không có dấu ngoặc nhọn kết thúc tương ứng, gây ra lỗi cú pháp.
3.2.8 Lists of JSX objects

Một chiến thuật phổ biến trong các React elements là ánh xạ một mảng các elements thành một mảng các đối tượng JSX để trả về trong một component. Hãy nói chúng ta muốn tạo một thành phần để hiển thị một danh sách thả xuống. Chúng ta muốn truyền list of options trong danh sách thả xuống dưới dạng một mảng chuỗi cho một thành phần <Select /> mới. Chúng ta muốn có khả năng thực hiện điều sau trong ứng dụng của chúng ta:
class App extends Component {
  render() {
    const items = ['apples', 'pears', 'playstations'];
    return <Select items={items} />;
  }
}
Sau đó, Select component của chúng ta nên đúng cách hiển thị một <select> với các phần tử <option> trong HTML. Chúng ta sẽ làm điều đó như thế nào? Cách ngây thơ nhất là đơn giản ánh xạ các phần tử từ chuỗi thành đối tượng JSX bằng cách sử dụng declarative programming, như thể hiện trong đoạn mã tiếp theo.
Listing 3.10 Naive implementation of select

import { Component } from "react";

class App extends Component {
  render() {
    const items = ["apples", "pears", "playstations"];
    return <Select items={items} />;
  }
}

class Select extends Component {
  render() {
    return (
      <select>
        {this.props.items.map((item) => (
           <option>{item}</option>
        ))}
      </select>
    );
  }
}
export default App;



Repository: rq03-naive-select
$ npx create-react-app rq03-naive-select --template rq03-naive-select
https://rq2e.com/rq03-naive-select
Đây là một cố gắng khá tốt để giải quyết vấn đề này. Tuy nhiên, nếu chúng ta chạy mã này trong trình duyệt, chúng ta sẽ nhận được một cảnh báo:
"Warning: Each child in a list should have a unique 'key' prop."
Ứng dụng vẫn hoạt động, nhưng chúng ta nhận được cảnh báo về việc thiếu thuộc tính key. Việc sử dụng thuộc tính key là một chút phức tạp ở giai đoạn này trong quá trình học React của chúng ta, nhưng nó được React sử dụng để theo dõi track xem cùng một element có di chuyển trong DOM được hiển thị hay không. Nếu cùng một element moves around, React sẽ tái sử dụng cùng một phần tử, nhưng nếu React không biết liệu đó có phải là cùng một phần tử hay không, React sẽ xóa tất cả các phần tử cũ và tạo ra hoàn toàn các phần tử mới mỗi khi danh sách render.

Đối với mục đích của ví dụ này, chúng ta có thể sử dụng giá trị của item như là key property trên phần tử gốc được trả về bên trong mảng được ánh xạ. Điều này dẫn đến mã nguồn như được thể hiện trong đoạn mã tiếp theo.

Listing 3.11 Correct implementation of select
import { Component } from "react";

class App extends Component {
  render() {
    const items = ["apples", "pears", "playstations"];
    return <Select items={items}></Select>
  }
}

class Select extends Component {
  render() {
    return (
      <select>
        {this.props.items.map((item) => (
          <option key={item}>{item}</option>
        ))}
      </select>
    );
  }
}

export default App;
Thuộc tính "key" là một thuộc tính nội bộ của React và sẽ không bao giờ được hiển thị trên DOM. Được khuyến nghị rằng thuộc tính "key" nên là một định danh duy nhất cho phần tử cụ thể đó, không chỉ là chỉ số của phần tử trong mảng (nếu các phần tử di chuyển trong mảng, các chỉ số thay đổi mặc dù các phần tử không thay đổi, nên việc tái sử dụng phần tử đúng cách bị đánh lừa).
Các key phải là duy nhất. Nếu bạn hiển thị một danh sách với các key không duy nhất, bạn sẽ nhận được một cảnh báo khác trong console về sự trùng lặp của các khóa.
LƯU Ý: Các key chỉ địa phương trong mảng cụ thể, vì vậy chúng chỉ cần phải là duy nhất trong từng mảng, không cần thiết phải duy nhất giữa tất cả các mảng trong ứng dụng hoặc thậm chí là giữa các thành phần. Các mảng khác nhau của các đối tượng JSX có thể có các khóa trùng lặp giữa chúng miễn là không có mảng nào có các khóa trùng lặp bên trong nó.

Như đã đề cập, đây là một tính năng của React khá phức tạp để hiểu ở giai đoạn này, vì vậy, tạm thời, chỉ cần biết rằng nếu bạn nhận được một cảnh báo trong console về việc thiếu thuộc tính "key" hoặc khóa trùng lặp, đó là nguyên nhân.
3.2.9 Fragments in JSX
Chúng ta đã đề cập đến JSX fragments một vài lần rồi. Chúng được sử dụng để xuất nhiều phần tử cùng mức độ trong tình huống chỉ cho phép một phần tử duy nhất. Trước đó, chúng ta đã thực hiện một điều tương tự để bao gồm cả tiêu đề và một liên kết:
import { Fragment } from 'react';
...
return (
  <Fragment>
    <h1>Hello and welcome</h1>
    <a href="/blog">Go to the blog</a>
  </Fragment>
);
Tuy nhiên, từ React 16.2 (và Babel 7) trở đi, một cú pháp ngắn hơn cũng được cho phép. Bây giờ
bạn thậm chí không cần phải nhập Fragment component:
return (
<> 
  <h1>Hello and welcome</h1>
  <a href="/blog">Go to the blog</a>
</>
);

Cú pháp ngắn này sử dụng một thẻ trống rỗng để render fragments. Tuy nhiên, cú pháp này với `<></>` không thể chứa bất kỳ thuộc tính hoặc thuộc tính nào. Thuộc tính duy nhất bạn có thể muốn áp dụng cho nó có thể là key vì bạn đang render một danh sách các phần tử, mỗi phần tử có nhiều hơn một phần tử JSX duy nhất ở mức gốc.
Một tình huống cổ điển cho điều này là một danh sách định nghĩa. Nó được định nghĩa trong HTML như sau:
<dl>
  <dt>Term A</dt>
  <dd>Description of Term A.</dd>
  <dt>Term B</dt>
  <dd>Description of Term B.</dd>
</dl> 
Như bạn có thể thấy, mỗi mục yêu cầu hai phần tử anh em trong danh sách để render (<dt> và <dd>).
Ví dụ, nếu chúng ta tạo một ứng dụng để render ba giống chó với mô tả ngắn về mỗi giống, chúng ta cần ánh xạ tên và định nghĩa của giống chó của mình vào hai phần tử. Chúng ta làm điều đó bằng cách bao quanh chúng bằng một đoạn văn, nhưng vì chúng ta cần đoạn văn có thuộc tính key, chúng ta phải sử dụng literal Fragment component, và, thật không may, không thể sử dụng cú pháp ngắn đã đề cập trước đó. Hãy thực hiện điều này trong đoạn mã dưới đây.


Listing 3.12 Definition list of dog breeds
import { Component, Fragment } from "react";

class App extends Component {
  render() {
    const list = [
      { breed: "Chihuahua", description: "Small breed of dog."},
      { breed: "Corgi", description: "Cute breed of dog." },
      { breed: "Cumberland Sheepdog", description: "Extinct breed of dog."},
    ];
    return <Breeds list={list}></Breeds>
  }
}

class Breeds extends Component {
  render() {
    return (
      <dl>
        {this.props.list.map(
          ({breed, description}) => (
            <Fragment key={breed}>
              <dt>{breed}</dt>
              <dt>{description}</dt>
            </Fragment>
          ))
        }
      </dl>
    );
  }
}

export default App;

Repository: rq03-dog-breeds
$ npx create-react-app rq03-dog-breeds --template rq03-dog-breeds
https://rq2e.com/rq03-dog-breeds

Nếu chúng ta chạy điều này trong trình duyệt, chúng ta sẽ có một danh sách định nghĩa đẹp đúng như chúng ta muốn, như bạn có thể thấy trong hình 3.4. Việc sử dụng các đoạn văn với khóa không phải là một trường hợp ngoại lệ như có vẻ, vì vậy điều này rất hữu ích để biết ngay từ giai đoạn này.’
 
Bây giờ bạn đã trải qua JSX và những lợi ích của nó. Phần còn lại của chương này được dành cho các công cụ JSX và những cạm bẫy tiềm ẩn cần tránh - đúng vậy: công cụ tools và điều cần lưu ý gotchas.
Trước khi chúng ta tiếp tục, bạn phải hiểu rằng để bất kỳ dự án JSX nào hoạt động đúng cách, JSX cần được biên dịch. Trình duyệt không thể chạy JSX trực tiếp - chúng chỉ có thể chạy JavaScript. Vì vậy, bạn cần lấy mã JSX và biên dịch nó thành JavaScript thông thường (xem hình 3.1). May mắn thay, nhiệm vụ đó không phức tạp như nó nghe có vẻ.
3.3 How to transpile JSX
Đối với tất cả các dự án và ví dụ trong cuốn sách này, bạn không cần thiết lập trình biên dịch riêng của mình (hoặc hầu hết các phần khác trong ngăn xếp công nghệ của bạn). Điều tương tự cũng đúng đối với hầu hết các dự án mà bạn sẽ gặp ngoài thực tế, vì các dự án hiện tại đã có một đường ống làm việc, và các dự án mới có thể dựa trên tài liệu thực hành tốt nhất được cung cấp bởi bất kỳ framework nào mà bạn muốn làm việc.
Tuy nhiên, nếu bạn muốn thiết lập một dự án React từ đầu, bạn có thể làm điều đó và điều đó bao gồm việc thiết lập một trình biên dịch JSX. Công cụ phổ biến nhất để biên dịch JSX là Babel, nhưng cũng có các lựa chọn khác mà bạn có thể muốn xem xét. Một số lựa chọn có thể là một phần của một gói công cụ xây dựng lớn hơn giúp việc thiết lập của bạn dễ dàng hơn hoặc đơn giản là thay thế thả vào cho Babel. Các lựa chọn khác bao gồm SWC, Sucrase và esbuild. Vui lòng tham khảo tài liệu của họ để biết chi tiết về cách sử dụng:

- Babel: https://babeljs.io/
- SWC: https://swc.rs/
- Sucrase: https://sucrase.io/
- esbuild: https://esbuild.github.io/

Chúng tôi mạnh mẽ khuyến khích bạn không nên dành quá nhiều thời gian để tạo ra một cấu hình trình biên dịch JSX cho riêng bạn. Những người tận tâm tại React đã tạo ra CRA (Create React App) cho chúng ta, nó sẽ phục vụ hầu hết các nhu cầu của chúng ta trong cuốn sách này. Bạn có thể muốn tìm hiểu về các thiết lập tùy chỉnh trong các dự án của bạn, nhưng đối với cuốn sách này, bạn sẽ được bảo vệ bởi các cài đặt được cung cấp bởi bộ công cụ tuyển chọn của chúng tôi.
3.4 React and JSX gotchas
Phần này bao gồm một số trường hợp ngoại lệ và điều kỳ cục mà bạn nên biết khi sử dụng JSX:
 **Self-closing tags là bắt buộc cho các leaf nodes.**
// Đúng
<img src="image.jpg" alt="Description" />
// Sai
<img src="image.jpg" alt="Description"></img>

 **Các ký tự đặc biệt được viết theo literally.**
// Đúng
<p>This is &lt;div&gt; element.</p>
// Sai
<p>This is <div> element.</p>

 **Chuyển đổi chuỗi có chút đặc biệt.**

 **Thuộc tính style là một đối tượng.**
// Đúng
<div style={{ color: 'red', fontSize: '16px' }}>Styled text</div>
// Sai
<div style="color: red; font-size: 16px;">Styled text</div>

**Một số thuộc tính có tên dự trữ reserved names và phải được đổi tên.**
// Đúng
<label htmlFor="inputField">Username:</label>
// Sai
<label for="inputField">Username:</label>

 **Các thuộc tính nhiều từ được viết theo kiểu camelCase.**
// Đúng
<div className="containerBox">Content</div>
// Sai
<div class="containerBox">Content</div>

 **Thuộc tính boolean được xử lý khác so với trong HTML.**
// Đúng
<input type="text" disabled={true} />
// Sai
<input type="text" disabled />

 **Một số khoảng trắng bị thu gọn (nhưng không phải tất cả).**
// Đúng
<div>  This text has intentional spaces.  </div>
// Sai
<div>This text has intentional spaces.</div>

 **Bạn có thể thêm các thuộc tính data- theo ý muốn.**
// Đúng
<div data-customAttribute="value">Content</div>
// Sai
<div customAttribute="value">Content</div>
3.4.1 Self-closing elements

JSX yêu cầu bạn phải có dấu gạch chéo (/) đóng ở cuối thẻ đóng closing tag hoặc, nếu bạn không có bất kỳ children nào, ở cuối thẻ đơn đó. Ví dụ, đây là cách đúng:
<a href="//react.dev">React</a>
<img src="/logo.png" alt="Logo" />

Còn đoạn mã sau đây là không đúng, vì cả hai node đều thiếu thẻ đóng:
<a href="//react.dev">React
<img src="/logo.png" alt="Logo">

Bạn có thể biết rằng HTML linh hoạt hơn. Trình duyệt sẽ bỏ qua dấu gạch chéo (/) hoặc phần kết thúc thiếu và vẫn hiển thị phần tử mà không có vấn đề gì. Hãy thử tạo một tệp HTML chỉ với `<button>Press me` và kiểm tra xem nút vẫn hiển thị đúng không!

3.4.2 Special characters
Các thực thể HTML là mã mà hiển thị các ký tự đặc biệt như ký hiệu bản quyền, dấu gạch dài, dấu ngoặc kép, và nhiều thứ khác. Dưới đây là một số ví dụ:
&copy;
&mdash;
&ldquo;

Bạn có thể hiển thị các mã này như bất kỳ chuỗi nào trong nội dung văn bản bên trong một node hoặc như một attribute của một node. Ví dụ, đây là JSX tĩnh (văn bản được defined trong mã mà không có biến hoặc thuộc tính):
<span>&copy;&mdash;&ldquo;</span>
<input value="&copy;&mdash;&ldquo;" />

Nhưng nếu bạn muốn dynamically output các thực thể HTML (từ một variable hoặc một property), bạn chỉ nhận được đầu ra trực tiếp (tức là `&copy;&mdash;&ldquo;`), không phải là các ký tự đặc biệt. Do đó, đoạn mã sau đây sẽ không hoạt động:

// Anti-pattern. Will NOT work!
const specialChars = '&copy;&mdash;&ldquo;'
<span>{specialChars}</span>
<input value={specialChars}/>
React/JSX sẽ tự động thoát HTML nguy hiểm, điều này là thuận tiện về mặt bảo mật (mặc định an toàn!). Để xuất các ký tự đặc biệt, bạn cần sử dụng một trong những phương pháp sau đây:

- Sao chép ký tự đặc biệt trực tiếp vào mã nguồn của bạn. Chỉ cần đảm bảo bạn sử dụng bảng mã UTF-8. Đây là phương pháp được khuyến khích để xử lý các ký tự đặc biệt.
- Thoát ký tự đặc biệt bằng \u và sử dụng số Unicode của nó (sử dụng một trang web như fileformat.info để tra cứu).
- Chuyển đổi từ mã ký tự thành số ký tự với String.fromCharCode(charCodeNumber).
- Sử dụng thuộc tính đặc biệt dangerouslySetInnerHTML để đặt HTML bên trong (điều này nguy hiểm và không được khuyến khích).
Để minh họa phương pháp cuối cùng (như một phương pháp dự phòng - khi mọi thứ đều thất bại trên tàu Titanic, hãy chạy đến thuyền!), xem xét đoạn mã sau:

const specialChars = '&copy;&mdash;&ldquo;';
<span dangerouslySetInnerHTML={{__html: specialChars}} />

Rõ ràng, đội ngũ React có tính hài hước khi đặt tên một thuộc tính là dangerouslySetInnerHTML.

3.4.3 String conversion

Khi React xuất outputs giá trị của variable hoặc biểu thức của bạn, nó sẽ được hiển thị như thế nào? Nó chỉ có thể hiển thị dưới dạng một trong hai điều: hoặc là một chuỗi, trở thành nội dung chuỗi giữa các phần tử, hoặc là một phần tử, sau đó chỉ trở thành một phần tử như nếu nó được hiển thị trực tiếp. Nhưng làm thế nào "các thứ" được chuyển đổi thành chuỗi nếu chúng không phải là một phần tử? Tốt, React ở đây có chút đặc biệt vì nó phụ thuộc vào loại biểu thức bạn đang hiển thị. Hãy nhìn vào bảng 3.2 để hiểu các khả năng cho các giá trị nguyên thủy khác nhau trong JavaScript.
Table 3.2 React rendering different types

"string": "string"
"": ""
3.4: "3.4"
0: "0"
NaN: "NaN"
Number.POSITIVE_INFINITY: "Infinity"
Number.NEGATIVE_INFINITY: "-Infinity"
true: "true"
false: ""
undefined: ""
null: ""
Có một vài điều bất ngờ ở đó. Quan trọng nhất, giá trị false trở thành chuỗi rỗng, nhưng giá trị true trở thành "true". Do đó, bốn giá trị falsy (chuỗi rỗng, false, null và undefined) đều trở thành chuỗi rỗng.
Nhưng còn về 0, cũng là giá trị falsy? Thì nó trở thành 0. Điều này sẽ là kỳ lạ nếu bạn không thể render một 0 trong các components của bạn, vì vậy điều này là cần thiết. Cuối cùng, NaN cũng chỉ là "NaN", không phải là chuỗi rỗng. Điều này giúp bạn dễ dàng gỡ lỗi tính toán của mình hơn - nếu bạn thấy một NaN, bạn biết bạn đã mắc lỗi ở đâu đó, nhưng nếu bạn chỉ thấy không có gì, bạn có thể không tìm thấy nó nhanh chóng.

Sự thực này - rằng false không hiển thị gì cả, nhưng 0 hiển thị một cái gì đó - quan trọng đặc biệt khi sử dụng toán tử AND logic để hiển thị các phần tử tùy chọn như chúng ta đã thảo luận trước đó. Bạn có thể quen với cách làm như sau trong JavaScript:
if (items.length) {
  hasItems = true;
}
Ở đây, chúng ta chỉ sử dụng `items.length` làm điều kiện cho câu lệnh if vì chúng ta biết rằng 0 là falsy, vì vậy chúng ta không cần nói `items.length > 0` - giá trị đúng của câu lệnh là giống nhau.

Tuy nhiên, bạn không nên làm điều này trong JSX. Giả sử bạn muốn hiển thị một nút Checkout trong giỏ hàng của bạn nếu nó chứa ít nhất một sản phẩm, nhưng bạn muốn không hiển thị gì khi giỏ hàng không có sản phẩm:
class ShoppingCart extends Component {
  render() {
      return (
          <aside>
              <h1>Shopping cart</h1>
              <CartItems items={this.props.items} />
              {this.props.items.length && (
                  <button>Checkout</button>
              )}
          </aside>
      );
  }


Điều này hoạt động miễn là có nhiều hơn 0 sản phẩm trong giỏ hàng. Nhưng điều gì sẽ xảy ra khi không có sản phẩm nào? Biểu thức AND logic được đánh dấu trong chú thích sẽ ngắn mạch và trả về giá trị falsy đầu tiên. Thêm vào đó, vì độ dài của mảng là 0, giá trị kết quả của biểu thức là đột ngột là 0, mà hiển thị là "0" trong tài liệu, như đã hiển thị trước đó trong bảng 3.2. Do đó, nếu bạn sử dụng mã chỉ định, giỏ hàng mua sắm trống rỗng của bạn sẽ đột ngột hiển thị một "0" ở dưới cùng của thành phần, làm mọi người nhầm lẫn.

Để triển khai đúng, luôn so sánh độ dài của mảng với 0 để đảm bảo kiểu là Boolean. Hơn nữa, bạn có thể lưu trữ so sánh đó trong một biến khác, làm mã trở nên đơn giản hơn để đọc:
class ShoppingCart extends Component {
  render() {
    const hasItems = this.props.items.length > 0;
    return (
      <aside>
        <h1>Shopping cart</h1>
        <CartItems items={this.props.items} />
        {hasItems && <button>Checkout</button>}
      </aside>
    );
  }
}

Không phải là hiếm khi quên điều này khi bạn đang phát triển, vì vậy việc phát hiện ra những số 0 lạ trong ứng dụng của bạn là hoàn toàn có thể. Chúng thường xuyên là kết quả của loại biểu thức này.

3.4.4 The style attribute

Thuộc tính style trong JSX hoạt động khác biệt so với HTML thông thường. Trong JSX, thay vì một chuỗi, bạn cần truyền một JavaScript object và các thuộc tính CSS cần được viết theo kiểu camelCase. Ví dụ:
- `background-image` trở thành `backgroundImage`.
- `font-size` trở thành `fontSize`.
- `font-family` trở thành `fontFamily`.
Bạn có thể lưu đối tượng JavaScript trong một var hoặc hiển thị nó trực tiếp với cặp dấu ngoặc nhọn kép (`{{...}}`). Dấu ngoặc nhọn kép là cần thiết vì một bộ là cho JSX và bộ kia là cho đối tượng chữ ký JavaScript.
Giả sử bạn có một đối tượng với kích thước phông chữ như sau:
const smallFontSize = { fontSize: '10pt' };

Trong JSX của bạn, bạn có thể sử dụng đối tượng `smallFontSize` như sau:
<input style={smallFontSize} />

Hoặc bạn có thể chọn một kích thước phông chữ lớn hơn (30 point) bằng cách truyền giá trị trực tiếp mà không cần một biến phụ trợ:
<input style={{ fontSize: '30pt' }} />

Hãy xem một ví dụ khác về việc truyền các kiểu trực tiếp. Lần này, bạn đang thiết lập một đường viền đỏ cho một `<span>`:

<span style={{
  borderWidth: '1px',
  borderStyle: 'solid',
  borderColor: 'red',
}}>Bánh red velvet thật ngon</span>

Hoặc giá trị đường viền sau cũng sẽ hoạt động và thực hiện cùng một công việc:
<span style={{ border: '1px red solid' }}>Hey</span>
Lý do chính làm sao các kiểu không phải là chuỗi CSS mà là đối tượng JavaScript là để React có thể làm việc với chúng nhanh chóng khi áp dụng các thay đổi cho các hiển thị.

3.4.5 Reserved names: class and for

3.4.6 Multiword attributes

Trong cùng tinh thần như hai tên đã được đề cập trong phần trước, một số thuộc tính HTML khác cũng được đổi tên trong React. Một số thuộc tính có ý nghĩa, nhưng một số khác thì không.
Bất kỳ thuộc tính nào được tạo từ hơn một từ tiếng Anh đều được đổi tên theo kiểu camelCase. Điều này hợp lý cho các thuộc tính scalable vector graphics (SVG) sử dụng dấu gạch ngang như clip-path hoặc fill-opacity. Chúng ta không thể sử dụng các thuộc tính có dấu gạch ngang trực tiếp trong JSX, nên chúng được đổi tên thành clipPath và fillOpacity tương ứng.
Tuy nhiên, điều tương tự cũng áp dụng cho các thuộc tính HTML không sử dụng dấu gạch ngang nhưng thường được viết thường, điều này có thể gây nhầm lẫn. Nếu bạn nhập:
return <video autoplay>...</video>;
Trong JSX, điều này sẽ không hoạt động vì, trong khi thuộc tính được gọi là autoplay (và có thể là chữ thường trong HTML), bạn phải sử dụng kiểu camelCase và gọi nó là autoPlay trong React. Điều này có thể gây khá nhiều khó chịu. Điều này cũng áp dụng cho một số lượng lớn các thuộc tính mà bạn thường xuyên sử dụng trong HTML.
Thay vì cảnh báo bạn về việc bỏ qua các thuộc tính này, React chỉ đơn giản lọc chúng một cách yên tĩnh. Do đó, bạn có thể không bao giờ biết rằng bạn đã nhập sai cho đến khi bạn nhận ra rằng video của bạn không tự động phát (vì autoPlay thay vì autoplay), iframe của bạn không cho phép chế độ toàn màn hình (vì allowFullscreen thay vì allowfullscreen), hoặc trường nhập của bạn không có giới hạn số ký tự được phép (vì max-Length thay vì maxlength).
3.4.7 Boolean attribute values

Một số thuộc tính (ví dụ: disabled, required, checked, autoFocus và readOnly) chỉ đặc biệt dành cho các phần tử form. Điều quan trọng nhất cần nhớ ở đây là giá trị thuộc tính phải được đặt là một biểu thức JavaScript (tức là bên trong {}) và không được đặt là một chuỗi. Ví dụ, sử dụng {false} để bật chế độ disabled cho ô nhập liệu:

<input disabled={false} />

Nhưng đừng sử dụng giá trị "false" vì nó sẽ qua kiểm tra truthy (một chuỗi không rỗng là truthy trong JavaScript, như bạn hy vọng nhớ từ phần 3.2.6). Điều này là do chuỗi "false" không phải là một trong sáu giá trị falsy; nó thực sự là một chuỗi không rỗng, nó là truthy và dẫn đến giá trị true. React sẽ hiển thị ô nhập liệu như đã bị vô hiệu hóa (disabled sẽ được đặt là true):
<input disabled="false" /> // Không làm như thế này!
Nếu bạn bỏ qua giá trị sau một thuộc tính, React sẽ đặt giá trị là true:
<input required />

Điều này tương đương với việc thiết lập giá trị thành true một cách thủ công, vì vậy chỉ cần sử dụng mã trước đó thay vì sử dụng required={true}.

Đối với nhiều thuộc tính trong HTML, việc loại bỏ hoàn toàn giá trị có nghĩa là đặt giá trị là false, vì vậy nếu bạn muốn đặt một giá trị cụ thể là true hoặc false, chỉ cần bao gồm nó mà không có giá trị hoặc bỏ qua nó. Nếu bạn muốn đặt giá trị dựa trên nội dung của một biến, hãy sử dụng một biểu thức:
<input readOnly={!isEditable} />

Lưu ý về vấn đề với từ ngữ đa từ đã được đề cập trước đó. Thuộc tính Boolean này trong React được gọi là readOnly và không phải là readonly như bạn biết từ HTML.

CUSTOM COMPONENT WITH BOOLEAN PROPERTIES
Điều tương tự cũng đúng khi bạn tạo các component của riêng mình. Nếu bạn có một custom component và muốn chấp nhận một thuộc tính Boolean, bạn chỉ cần sử dụng một thuộc tính từ this.props như nó là một Boolean, và React sẽ đảm bảo đặt nó thành true nếu được chỉ định khi sử dụng.

Ví dụ, chúng ta có thể tạo một thành phần cảnh báo sẽ hiển thị một thông báo cho người dùng. Thông báo này có thể là lỗi hoặc cảnh báo. Để kiểm soát mức độ của thông báo, chúng ta thêm một cờ Boolean, isError, và nếu là true, chúng ta bao gồm biểu tượng cảnh báo xung quanh thông báo. Sau đó, chúng ta sẽ sử dụng thành phần này để hiển thị hai thông báo khác nhau trong ứng dụng của chúng ta - một làm lỗi và một làm cảnh báo, như được hiển thị trong đoạn mã 3.13.

import { Component } from 'react';
class Alert extends Component {
  render() {
    return (
      <p>
        {this.props.isError && '⚠'}
        {this.props.children}
        {this.props.isError && '⚠'}
      </p>
    );
  }
}
class App extends Component {
  render() {
    return (
     <main>
        <Alert>We are almost out of cookies</Alert>
        <Alert isError>
          We are completely out of ice cream
        </Alert>
      </main>
    );
  }
}
export default App;

Nếu chúng ta chạy điều này trong trình duyệt, chúng ta sẽ thấy cách hai thông báo được hiển thị đúng (xem hình 3.5).
 

3.4.8 Whitespace

Nếu bạn muốn thêm khoảng trắng giữa các components - ví dụ, nếu bạn đang thêm một từ in đậm trong một câu - bạn phải rất cẩn trọng về cách bạn đặt ký tự xuống dòng của mình. Hãy nói bạn muốn viết một tiêu đề với một từ được nhấn mạnh ở giữa, ví dụ, "All corgis are awesome " nhưng "corgis" phải được in nghiêng. Bạn có thể làm điều này trong JSX như được hiển thị trong đoạn mã tiếp theo.

Listing 3.14 Naive implementation of a partially emphasized message

import { Component } from 'react';
class App extends Component {
  render() {
    return (
      <h1>
        All
        <em>corgis</em>
        are awesome
      </h1>
    );
  }
}
export default App;
Repository: rq03-bad-whitespace
$ npx create-react-app rq03-bad-whitespace --template rq03-bad-whitespace
https://rq2e.com/rq03-bad-whitespace
Có vẻ khá hợp lý, phải không? Hãy chạy ứng dụng này với CRA và xem nó trên trình duyệt. Bạn có thể xem kết quả trong hình 3.6.

 

Điều đó rõ ràng là không đúng. Khoảng trắng xung quanh từ "corgis" đơn giản bị thu gọn. Điều gì đã xảy ra?
Thường, các ký tự xuống dòng và tab đều bị bỏ qua như là khoảng trắng trong JSX. Khi chúng ta có JSX như
return (
  <main>
    <h1>Hello world</h1>
  </main>
);
ở phần đầu chương, chúng ta thực sự không muốn có khoảng trắng giữa các phần tử `<main>` và `<h1>`. Chúng ta chỉ định dạng nó trên nhiều dòng vì nó trông đẹp - không phải vì chúng ta muốn có nhiều khoảng trắng thừa được hiển thị trong trình duyệt. Vì vậy, nếu có khoảng trắng giữa các phần tử trong JSX bao gồm các ký tự xuống dòng, tất cả các khoảng trắng đó sẽ bị thu gọn. Điều này không quan trọng nếu bạn có một khoảng trắng bình thường thêm vào cuối dòng văn bản thông thường trong đoạn mã 3.14. Nếu có một ký tự xuống dòng giữa các phần tử, tất cả các khoảng trắng sẽ bị thu gọn.

Vậy làm thế nào để làm điều này đúng? Có hai cách để đảm bảo các khoảng trắng được hiển thị:
- Không sử dụng ký tự xuống dòng giữa các phần tử.
- Thêm các khoảng trắng như là các biểu thức trong mã.
Cách thứ hai nghe có vẻ phức tạp và không trông mấy tốt, nhưng có thể cần thiết. Hãy xem xét giải pháp đầu tiên - không có ký tự xuống dòng - trong thực tế.
Listing 3.15 Partially emphasized message without newline characters
import { Component } from 'react';
class App extends Component {
  render() {
    return (
      <h1>
        All <em>corgis</em> are awesome
      </h1>
    );
  }
}
export default App;
Lưu ý rằng chúng ta có thể có ký tự xuống dòng trước và sau message (vì khoảng trắng ở đây có thể bị thu gọn - chúng ta không quan tâm đến nó). Chúng ta chỉ không muốn có ký tự xuống dòng ở những nơi chúng ta muốn có các ký tự khoảng trắng thực sự được chèn vào. Bây giờ hãy xem xét các biểu thức khoảng trắng trong đoạn mã tiếp theo.
Listing 3.16 Partially emphasized message with space expressions
import { Component } from 'react';
class App extends Component {
  render() {
    return (
      <h1>
        All
        {" "}
        <em>corgis</em>
        {" "}
        are awesome
      </h1>
    );
  }
}
export default App;

Ở đây, chúng ta thêm các khoảng trắng bằng cách sử dụng {}. Điều này sẽ buộc JSX engine bao gồm các khoảng trắng như là các element thực sự và không xem chúng như là một phần của khoảng trắng không đáng kể mà thường tồn tại giữa các phần tử. Bạn thường sẽ thấy các nhà phát triển thêm các biểu thức khoảng trắng như vậy vào cuối dòng trước ký tự xuống dòng, như được hiển thị ở đây.

3.4.9 data- attributes
Đôi khi, bạn muốn truyền thêm dữ liệu bằng cách sử dụng các DOM nodes. Mặc dù bạn không nên sử dụng DOM của mình như một cơ sở dữ liệu hoặc local storage, đôi khi điều đó là cần thiết khi bạn muốn truyền biến var cho các thư viện của bên thứ ba. Nếu bạn cần tạo các thuộc tính tùy chỉnh và muốn chúng được hiển thị, hãy sử dụng tiền tố data-.

Ví dụ, đây là một thuộc tính tùy chỉnh hợp lệ với tên data-object-id mà React sẽ hiển thị trong giao diện (HTML sẽ giống như JSX này):
<li data-object-id={object.id}>...</li>
3.5 Quiz

1 To output a JavaScript variable in JSX, which of the following do you use? =, <%= %>, {}, or <?= ?>
2 The class attribute isn’t allowed in JSX. True or false?
3 The default value for an attribute without a value is false. True or false?
4 The inline style attribute in JSX is a JavaScript object and not a string like other
attributes. True or false?
5 If you need to have if/else logic in JSX, you can use it inside {}. For example,
class={if (!this.props.isAdmin) return 'hide'} is valid JSX code. True or
false?

Quiz answers
1 You use {} for variables and expressions.
2 True. class is a reserved JavaScript statement. For this reason, you use className in JSX.
3 False. The default value for a property with no value specified is true.
4 True. style is an object for performance reasons.
5 False. First, class isn’t the proper attribute name; it’s className. Then, instead
of if return (which isn’t valid JavaScript anyway in this context), you should
use a ternary operator or logical expressions. You could do it like this: className={this.props.isAdmin || 'hide'}.

Summary

- JSX chỉ là syntactic sugar cho các phương thức React như React.createElement.
- Bạn nên sử dụng className và htmlFor thay vì các thuộc tính class và for tiêu chuẩn của HTML.
- Thuộc tính style nhận một đối tượng JavaScript, không phải là một chuỗi như trong HTML thông thường.
- Toán tử ba ngôi và toán tử logic là cách tốt nhất để thực hiện các câu lệnh if/else.
- Việc output các variable, comments và các ký tự đặc biệt HTML là dễ dàng và trực tiếp.
- Một số thuộc tính HTML và SVG đa từ được đổi tên trong React, vì vậy hãy chú ý đến những thuộc tính đặc biệt này và nhớ kiểm tra xem liệu các thuộc tính của bạn có được đưa vào tài liệu HTML một cách chính xác hay không.
- JSX cần được biên dịch thành JavaScript trước khi có thể chạy trong trình duyệt, nhưng bạn hiếm khi phải lo lắng về điều đó. Tuy nhiên, nếu bạn cảm thấy cần thiết, có nhiều công cụ có sẵn, trong đó có Babel, là công cụ phổ biến nhất vào thời điểm viết lời.


