1. Test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```
CREATE TABLE employee(
id INTEGER,
name VARCHAR(50),
birthday DATE,
email VARCHAR(100)
)
```

2. Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```
insert into employee (id, name, birthday, email) values (1, 'Audrey Spinke', '16.4.1987', 'aspinke0@people.com.cn');
insert into employee (id, name, birthday, email) values (2, 'Cherin Darrington', '6.12.1971', 'cdarrington1@gizmodo.com');
insert into employee (id, name, birthday, email) values (3, 'Eada Andrejs', '2.2.1987', 'eandrejs2@upenn.edu');
insert into employee (id, name, birthday, email) values (4, 'Alyce Scotney', '29.1.2001', 'ascotney3@furl.net');
insert into employee (id, name, birthday, email) values (5, 'Venus Bockmaster', '2.7.2012', 'vbockmaster4@nymag.com');
insert into employee (id, name, birthday, email) values (6, 'Dianna Nortunen', '19.10.1968', 'dnortunen5@behance.net');
insert into employee (id, name, birthday, email) values (7, 'Inigo Willford', '28.10.2005', 'iwillford6@discuz.net');
insert into employee (id, name, birthday, email) values (8, 'Andria Doiley', '24.9.1992', 'adoiley7@abc.net.au');
insert into employee (id, name, birthday, email) values (9, 'Alicia Glaum', '2.7.2012', 'aglaum8@joomla.org');
insert into employee (id, name, birthday, email) values (10, 'Beilul Sanbrook', '3.4.1963', 'bsanbrook9@unc.edu');
insert into employee (id, name, birthday, email) values (11, 'Pierson Cullin', '27.6.1974', 'pcullina@furl.net');
insert into employee (id, name, birthday, email) values (12, 'Nevil Hanham', '14.6.1994', 'nhanhamb@weibo.com');
insert into employee (id, name, birthday, email) values (13, 'Corinne Schultze', '3.5.1965', 'cschultzec@sakura.ne.jp');
insert into employee (id, name, birthday, email) values (14, 'Kaitlynn De Beneditti', '2.12.1990', 'kded@bigcartel.com');
insert into employee (id, name, birthday, email) values (15, 'Aurelea Atmore', '7.8.1991', 'aatmoree@tinyurl.com');
insert into employee (id, name, birthday, email) values (16, 'Marketa Guiraud', '17.1.1973', 'mguiraudf@prnewswire.com');
insert into employee (id, name, birthday, email) values (17, 'Adrianne Dalwood', '19.5.1986', 'adalwoodg@vkontakte.ru');
insert into employee (id, name, birthday, email) values (18, 'Augustus Longstreet', '9.8.1988', 'alongstreeth@umn.edu');
insert into employee (id, name, birthday, email) values (19, 'Hinda Hepher', '14.3.2007', 'hhepheri@ucoz.ru');
insert into employee (id, name, birthday, email) values (20, 'Aggie Pedwell', '16.3.1987', 'apedwellj@umn.edu');
insert into employee (id, name, birthday, email) values (21, 'Gaspard Hartley', '2.4.2011', 'ghartleyk@stanford.edu');
insert into employee (id, name, birthday, email) values (22, 'Katalin Moylan', '28.5.2012', 'kmoylanl@google.com.hk');
insert into employee (id, name, birthday, email) values (23, 'Johann Plaxton', '6.12.1981', 'jplaxtonm@msn.com');
insert into employee (id, name, birthday, email) values (24, 'Ortensia Cassley', '26.11.2011', 'ocassleyn@guardian.co.uk');
insert into employee (id, name, birthday, email) values (25, 'Bellina Elderbrant', '9.7.1977', 'belderbranto@cnn.com');
insert into employee (id, name, birthday, email) values (26, 'Lari Offener', '19.6.1979', 'loffenerp@phpbb.com');
insert into employee (id, name, birthday, email) values (27, 'Clea Covert', '25.6.1969', 'ccovertq@adobe.com');
insert into employee (id, name, birthday, email) values (28, 'Wells Kenwrick', '25.11.1985', 'wkenwrickr@miitbeian.gov.cn');
insert into employee (id, name, birthday, email) values (29, 'Courtney Dillamore', '14.2.1989', 'cdillamores@360.cn');
insert into employee (id, name, birthday, email) values (30, 'Field Whereat', '6.4.1964', 'fwhereatt@php.net');
insert into employee (id, name, birthday, email) values (31, 'Ketty Pawelec', '17.7.2009', 'kpawelecu@123-reg.co.uk');
insert into employee (id, name, birthday, email) values (32, 'Cesar Mingame', '18.9.2007', 'cmingamev@chronoengine.com');
insert into employee (id, name, birthday, email) values (33, 'Kala Burmaster', '26.4.1970', 'kburmasterw@adobe.com');
insert into employee (id, name, birthday, email) values (34, 'Merridie Hollidge', '5.3.2003', 'mhollidgex@parallels.com');
insert into employee (id, name, birthday, email) values (35, 'Pegeen Gulk', '21.1.1986', 'pgulky@vistaprint.com');
insert into employee (id, name, birthday, email) values (36, 'Jacquelynn Burgne', '23.2.1988', 'jburgnez@qq.com');
insert into employee (id, name, birthday, email) values (37, 'Sharon Lammerich', '2.3.2009', 'slammerich10@soundcloud.com');
insert into employee (id, name, birthday, email) values (38, 'Jeremias Chessum', '9.2.2006', 'jchessum11@europa.eu');
insert into employee (id, name, birthday, email) values (39, 'Boycey Courcey', '11.7.1955', 'bcourcey12@nhs.uk');
insert into employee (id, name, birthday, email) values (40, 'Gerik Leopard', '27.7.1965', 'gleopard13@chicagotribune.com');
insert into employee (id, name, birthday, email) values (41, 'Phylis Baunton', '5.10.1999', 'pbaunton14@pcworld.com');
insert into employee (id, name, birthday, email) values (42, 'Corabelle Palmby', '30.1.2003', 'cpalmby15@mlb.com');
insert into employee (id, name, birthday, email) values (43, 'Emerson Astridge', '15.3.1952', 'eastridge16@purevolume.com');
insert into employee (id, name, birthday, email) values (44, 'Liz Minghella', '17.10.1958', 'lminghella17@360.cn');
insert into employee (id, name, birthday, email) values (45, 'Cary Stapylton', '13.2.1979', 'cstapylton18@wiley.com');
insert into employee (id, name, birthday, email) values (46, 'Robinet Brikner', '11.7.1983', 'rbrikner19@fastcompany.com');
insert into employee (id, name, birthday, email) values (47, 'Carmine Hanstock', '17.10.2006', 'chanstock1a@facebook.com');
insert into employee (id, name, birthday, email) values (48, 'Reena Oatley', '22.1.1993', 'roatley1b@arstechnica.com');
insert into employee (id, name, birthday, email) values (49, 'Christel Greenhalf', '11.5.1976', 'cgreenhalf1c@mashable.com');
insert into employee (id, name, birthday, email) values (50, 'Dorella Winslade', '16.7.1977', 'dwinslade1d@parallels.com');
```

3. Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```
UPDATE employee
SET name = 'Ahmet Yılmaz', birthday = '1996-05-12', email = 'ahmet.yilmaz@gmail.com'
WHERE id = 15;

UPDATE employee
SET name = 'Hande Sezer', birthday = '1990-07-20', email = 'hande.sezer@gmail.com'
WHERE name LIKE 'Liz%';

UPDATE employee
SET name = 'Şükrü Aydın', birthday = '1988-03-27', email = 'sukru.aydin@gmail.com'
WHERE id = 1;

UPDATE employee
SET name = 'Pikachu', birthday = '1999-11-01', email = 'pikachu@pokemon.com'
WHERE email LIKE 'pc%';

UPDATE employee
SET name = 'x', birthday = '2000-01-01', email = '-'
WHERE id > 45
```

4. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```
DELETE FROM employee
WHERE id = 25;

DELETE FROM employee
WHERE name LIKE 'L%';

DELETE FROM employee
WHERE id < 5;

DELETE FROM employee
WHERE email LIKE 'A%';

DELETE FROM employee
WHERE name = 'x';
```

[Patika Dev Profilim](https://app.patika.dev/adamblue)

www.patika.dev

