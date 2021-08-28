---
description: 'дополнительные сведения: максимальное Параметры константы'
title: максимальное Параметры констант
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38184176e5803cfd22d7b63f9d85e5b62f7ecff1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478970"
---
# <a name="maximum-settings-constants"></a>максимальное Параметры констант


_**Применимо к:** Windows | Windows Сервером_

## <a name="maximum-settings-constants"></a>максимальное Параметры констант

Эти константы предоставляют максимальные параметры, разрешенные для элементов в базе данных ESE.


| <p>Константа/значение</p> | <p>Описание</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>Задает длину префикса, используемого для имен файлов, используемых ядром СУБД. Эта длина применима к имени, заданному для параметра системы <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>Задает максимальную длину для <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>Максимальный размер закладки по умолчанию. Это допустимо, если размер ключа остался равным значению по умолчанию.</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>Максимальный размер закладки, если для ESENT настроено максимально возможное количество ключей.</p><p><strong>Windows 7:</strong> JET_cbBookmarkMostMost представлен в Windows 7.</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>Максимальная длина имени объекта, столбца, индекса или свойства.</p><p><strong>Примечание</strong>  .  Если Unicode, значение равно 128.</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>Максимальная длина "name.name.name..." создания.</p><p><strong>Примечание</strong>  .  Если Unicode, значение равно 510.</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>Этот номер можно использовать для расчета максимального объема большого двоичного объекта, который может храниться ядром СУБД на одной странице базы данных. Формула имеет максимальный размер = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</p><p>Теперь это значение устарело. Размер фрагмента данных с длинным значением должен быть получен с помощью параметра JET_paramLVChunkSizeMost.</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>Максимальный размер данных в столбцах, не являющихся значениями типа long.</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>Максимальный размер значения по умолчанию для столбца длинных значений (Лонгбинари или LongText).</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>Максимальный размер ключа сортировки или индекса по умолчанию.</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>Максимальный настраиваемый размер ключа сортировки или индекса для любого размера страницы. (См. JET_INDEXCREATE2. Кбкэймост)</p><p><strong>Windows 7:</strong> JET_cbKeyMostMost введена в операционной системе Windows 7.</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 2048 байт. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage введены в операционную систему Windows Vista.</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1000</p> | <p>Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 4096 байт. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage введены в Windows Vista.</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 8192 байт. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista:</strong> JET_cbKeyMost8KBytePage появилось в Windows Vista</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>Минимальный допустимый максимальный размер ключа индекса. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista:</strong> JET_cbKeyMostMin введены в Windows Vista.</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>Максимальный размер ключа при формировании ключа с помощью ограничения <em>грбит</em>, например JET_bitStrLimit, которое используется в функции <a href="gg269329(v=exchg.10).md">жетмакекэй</a> .</p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>Максимальный размер первичного индекса. Эта возможность устарела.</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>Максимальный размер вторичного индекса. Эта возможность устарела.</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>Максимальное число компонентов в ключе сортировки или индекса.</p><p><strong>Windows Vista:</strong> в Windows Vista и более поздних версиях Windows значение равно 16.</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>Максимально допустимое число столбцов в таблице.</p><p><strong>Windows XP:</strong> значение 0x0000fee0 используется в Windows XP и более поздних версиях Windows</p><p><strong>Windows 2000:</strong> значение 0x00007ffe используется в Windows 2000.</p> | 
| <p>JET_ccolFixedMost<br />0x0000007F</p> | <p>Максимальное число фиксированных столбцов, разрешенное в таблице, в настоящее время 127.</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>Максимальное число столбцов переменной длины, которые могут содержаться в таблице, в настоящее время 128.</p> | 
| <p>JET_ccolTaggedMost<br />(JET_ccolMost-0x000000ff)</p> | <p>Максимальное число столбцов с тегами, которые могут содержаться в таблице, в настоящее время 64993.</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


