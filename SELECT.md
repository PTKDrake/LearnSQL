---


---

<h1 id="a-little-sql">A little SQL</h1>
<p><strong>Hỏ</strong></p>
<h1 id="select">SELECT</h1>
<h2 id="lấy-tất-cả-các-cột-từ-một-bảng">1.  Lấy tất cả các cột từ một bảng:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span>  <span class="token operator">*</span>  <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<p><strong>table_name</strong>: Tên bảng</p>
<h2 id="lấy-các-cột-cụ-thể-từ-một-bảng">2.  Lấy các cột cụ thể từ một bảng:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> column2<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<p><strong>column1</strong>, <strong>column2</strong>: Tên cột</p>
<h2 id="lấy-các-cột-cụ-thể-và-đổi-tên-cho-chúng">3.  Lấy các cột cụ thể và đổi tên cho chúng:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1 <span class="token keyword">AS</span> alias1<span class="token punctuation">,</span> column2 <span class="token keyword">AS</span> alias2<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<p>Cách rút gọn:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1 alias1<span class="token punctuation">,</span> column2 alias2<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<h2 id="lấy-các-cột-duy-nhất-từ-một-bảng-loại-bỏ-các-dòng-trùng-lặp">4.  Lấy các cột duy nhất từ một bảng (loại bỏ các dòng trùng lặp):</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">DISTINCT</span> column1<span class="token punctuation">,</span> column2<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<h2 id="lấy-các-dòng-dựa-trên-điều-kiện">5.  Lấy các dòng dựa trên điều kiện:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> table_name <span class="token keyword">WHERE</span> condition1 <span class="token operator">AND</span> condition2<span class="token punctuation">;</span>
</code></pre>
<p>Ex:</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> table_name <span class="token keyword">WHERE</span> id<span class="token operator">=</span><span class="token number">1</span> <span class="token operator">AND</span> name<span class="token operator">=</span><span class="token string">'Test'</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="sắp-xếp-kết-quả-tăng-dần">6.  Sắp xếp kết quả tăng dần:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> table_name <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">ASC</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="sắp-xếp-kết-quả-tăng-dần-1">7.  Sắp xếp kết quả tăng dần:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> table_name <span class="token keyword">ORDER</span> <span class="token keyword">BY</span> column1<span class="token punctuation">,</span> column2 <span class="token keyword">DESC</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="giới-hạn-số-lượng-kết-quả-trả-về">8.  Giới hạn số lượng kết quả trả về:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token keyword">TOP</span> n <span class="token operator">*</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<p><strong>n</strong>: Số lượng dòng kết quả muốn lấy</p>
<h2 id="bỏ-qua-một-số-dòng-ban-đầu-và-lấy-kết-quả-từ-dòng-thứ-n">9.  Bỏ qua một số dòng ban đầu và lấy kết quả từ dòng thứ n:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token operator">*</span> <span class="token keyword">FROM</span> table_name <span class="token keyword">OFFSET</span> n <span class="token keyword">ROWS</span><span class="token punctuation">;</span>
</code></pre>
<p><strong>n</strong>: số lượng dòng muốn bỏ qua.</p>
<h2 id="tính-tổng-các-giá-trị-của-một-cột">10.  Tính tổng các giá trị của một cột:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">SUM</span><span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<h2 id="tính-trung-bình-các-giá-trị-của-một-cột">11.  Tính trung bình các giá trị của một cột:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> <span class="token function">AVG</span><span class="token punctuation">(</span>column_name<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name<span class="token punctuation">;</span>
</code></pre>
<h2 id="nhóm-dữ-liệu-dựa-trên-giá-trị-của-một-cột">12.  Nhóm dữ liệu dựa trên giá trị của một cột:</h2>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> column1<span class="token punctuation">,</span> <span class="token function">COUNT</span><span class="token punctuation">(</span>column2<span class="token punctuation">)</span> <span class="token keyword">FROM</span> table_name <span class="token keyword">GROUP</span> <span class="token keyword">BY</span> column1<span class="token punctuation">;</span>
</code></pre>
<h2 id="sử-dụng-với-mệnh-đề-join">13. Sử dụng với mệnh đề JOIN</h2>
<p>Cho bảng “Orders”:</p>

<table>
<thead>
<tr>
<th align="left">OrderID</th>
<th align="left">CustomerID</th>
<th align="left">EmployeeID</th>
<th align="left">OrderDate</th>
<th align="left">ShipperID</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">10308</td>
<td align="left">2</td>
<td align="left">7</td>
<td align="left">1996-09-18</td>
<td align="left">3</td>
</tr>
<tr>
<td align="left">10309</td>
<td align="left">37</td>
<td align="left">3</td>
<td align="left">1996-09-19</td>
<td align="left">1</td>
</tr>
<tr>
<td align="left">10310</td>
<td align="left">77</td>
<td align="left">8</td>
<td align="left">1996-09-20</td>
<td align="left">2</td>
</tr>
</tbody>
</table><p>Cho bảng “Customers”:</p>

<table>
<thead>
<tr>
<th align="left">CustomerID</th>
<th align="left">CustomerName</th>
<th align="left">ContactName</th>
<th align="left">Country</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">1</td>
<td align="left">Alfreds Futterkiste</td>
<td align="left">Maria Anders</td>
<td align="left">Germany</td>
</tr>
<tr>
<td align="left">2</td>
<td align="left">Ana Trujillo Emparedados y helados</td>
<td align="left">Ana Trujillo</td>
<td align="left">Mexico</td>
</tr>
<tr>
<td align="left">3</td>
<td align="left">Antonio Moreno Taquería</td>
<td align="left">Antonio Moreno</td>
<td align="left">Mexico</td>
</tr>
</tbody>
</table><p>Cho bảng “Employees”:</p>

<table>
<thead>
<tr>
<th align="left">EmployeeID</th>
<th align="left">LastName</th>
<th align="left">FirstName</th>
<th align="left">BirthDate</th>
<th align="left">Photo</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">1</td>
<td align="left">Davolio</td>
<td align="left">Nancy</td>
<td align="left">12/8/1968</td>
<td align="left">EmpID1.pic</td>
</tr>
<tr>
<td align="left">2</td>
<td align="left">Fuller</td>
<td align="left">Andrew</td>
<td align="left">2/19/1952</td>
<td align="left">EmpID2.pic</td>
</tr>
<tr>
<td align="left">3</td>
<td align="left">Leverling</td>
<td align="left">Janet</td>
<td align="left">8/30/1963</td>
<td align="left">EmpID3.pic</td>
</tr>
</tbody>
</table><h3 id="inner-join">&lt;1&gt; INNER JOIN</h3>
<p><img src="https://www.w3schools.com/sql/img_innerjoin.gif" alt="SQL INNER JOIN"><br>
INNER JOIN kết hợp các dòng từ hai (hoặc nhiều) bảng dựa trên điều kiện kết hợp. Kết quả chỉ bao gồm các dòng có sự kết hợp giữa các bảng theo điều kiện được chỉ định.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> Orders<span class="token punctuation">.</span>OrderID<span class="token punctuation">,</span> Customers<span class="token punctuation">.</span>CustomerName<span class="token punctuation">,</span> Orders<span class="token punctuation">.</span>OrderDate  
<span class="token keyword">FROM</span> Orders  
<span class="token keyword">INNER</span>  <span class="token keyword">JOIN</span> Customers <span class="token keyword">ON</span> Orders<span class="token punctuation">.</span>CustomerID<span class="token operator">=</span>Customers<span class="token punctuation">.</span>CustomerID<span class="token punctuation">;</span>
</code></pre>
<p>Kết quả:</p>

<table>
<thead>
<tr>
<th align="left">OrderID</th>
<th align="center">CustomerName</th>
<th align="right">OrderDate</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">10308</td>
<td align="center">Ana Trujillo Emparedados y helados</td>
<td align="right">9/18/1996</td>
</tr>
</tbody>
</table><h3 id="left-join">&lt;2&gt; LEFT JOIN</h3>
<p><img src="https://www.w3schools.com/sql/img_leftjoin.gif" alt="SQL LEFT JOIN"><br>
LEFT JOIN trả về tất cả các dòng từ bảng bên trái (LEFT) và các dòng khớp từ bảng bên phải (RIGHT). Nếu không có sự khớp, các cột từ bảng bên phải sẽ có giá trị NULL trong kết quả.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> Customers<span class="token punctuation">.</span>CustomerName<span class="token punctuation">,</span> Orders<span class="token punctuation">.</span>OrderID  
<span class="token keyword">FROM</span> Customers  
<span class="token keyword">LEFT</span>  <span class="token keyword">JOIN</span> Orders <span class="token keyword">ON</span> Customers<span class="token punctuation">.</span>CustomerID <span class="token operator">=</span> Orders<span class="token punctuation">.</span>CustomerID  
<span class="token keyword">ORDER</span>  <span class="token keyword">BY</span> Customers<span class="token punctuation">.</span>CustomerName<span class="token punctuation">;</span>
</code></pre>
<p>Kết quả:</p>

<table>
<thead>
<tr>
<th align="left">CustomerName</th>
<th align="left">OrderID</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Alfreds Futterkiste</td>
<td align="left">null</td>
</tr>
<tr>
<td align="left">Ana Trujillo Emparedados y helados</td>
<td align="left">10308</td>
</tr>
<tr>
<td align="left">Antonio Moreno Taquería</td>
<td align="left">10365</td>
</tr>
</tbody>
</table><h3 id="right-join">&lt;3&gt; RIGHT JOIN</h3>
<p><img src="https://www.w3schools.com/sql/img_rightjoin.gif" alt="SQL RIGHT JOIN"><br>
RIGHT JOIN trả về tất cả các dòng từ bảng bên phải (RIGHT) và các dòng khớp từ bảng bên trái (LEFT). Nếu không có sự khớp, các cột từ bảng bên trái sẽ có giá trị NULL trong kết quả.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> Orders<span class="token punctuation">.</span>OrderID<span class="token punctuation">,</span> Employees<span class="token punctuation">.</span>LastName<span class="token punctuation">,</span> Employees<span class="token punctuation">.</span>FirstName<span class="token punctuation">,</span> Orders<span class="token punctuation">.</span>OrderID   
<span class="token keyword">FROM</span> Orders  
<span class="token keyword">RIGHT</span>  <span class="token keyword">JOIN</span> Employees <span class="token keyword">ON</span> Orders<span class="token punctuation">.</span>EmployeeID <span class="token operator">=</span> Employees<span class="token punctuation">.</span>EmployeeID  
<span class="token keyword">ORDER</span>  <span class="token keyword">BY</span> Orders<span class="token punctuation">.</span>OrderID<span class="token punctuation">;</span>
</code></pre>
<p>Kết quả:</p>

<table>
<thead>
<tr>
<th align="left">OrderID</th>
<th align="left">LastName</th>
<th align="left">FirstName</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Null</td>
<td align="left">Davolio</td>
<td align="left">Nancy</td>
</tr>
<tr>
<td align="left">Null</td>
<td align="left">Leverling</td>
<td align="left">Janet</td>
</tr>
<tr>
<td align="left">10309</td>
<td align="left">Leverling</td>
<td align="left">Janet</td>
</tr>
</tbody>
</table><h3 id="full-join">&lt;4&gt; FULL JOIN</h3>
<p><img src="https://www.w3schools.com/sql/img_fulljoin.gif" alt="SQL FULL OUTER JOIN"><br>
FULL JOIN trả về tất cả các dòng từ cả hai bảng (LEFT và RIGHT), bao gồm cả các dòng không khớp. Nếu không có sự khớp, các cột từ bảng không khớp sẽ có giá trị NULL trong kết quả.</p>
<pre class=" language-sql"><code class="prism  language-sql"><span class="token keyword">SELECT</span> Customers<span class="token punctuation">.</span>CustomerName<span class="token punctuation">,</span> Orders<span class="token punctuation">.</span>OrderID  
<span class="token keyword">FROM</span> Customers  
<span class="token keyword">FULL</span>  <span class="token keyword">OUTER</span>  <span class="token keyword">JOIN</span> Orders <span class="token keyword">ON</span> Customers<span class="token punctuation">.</span>CustomerID<span class="token operator">=</span>Orders<span class="token punctuation">.</span>CustomerID  
<span class="token keyword">ORDER</span>  <span class="token keyword">BY</span> Customers<span class="token punctuation">.</span>CustomerName<span class="token punctuation">;</span>
</code></pre>
<p>Kết quả:</p>

<table>
<thead>
<tr>
<th align="left">CustomerName</th>
<th align="left">OrderID</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Null</td>
<td align="left">10309</td>
</tr>
<tr>
<td align="left">Null</td>
<td align="left">10310</td>
</tr>
<tr>
<td align="left">Alfreds Futterkiste</td>
<td align="left">Null</td>
</tr>
<tr>
<td align="left">Ana Trujillo Emparedados y helados</td>
<td align="left">10308</td>
</tr>
<tr>
<td align="left">Antonio Moreno Taquería</td>
<td align="left">Null</td>
</tr>
</tbody>
</table>
