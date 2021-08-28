---
description: 'Дополнительные сведения: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: ee83dc86aa6faf5fab0b45596a586c657e4c6e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474130"
---
# <a name="jet_snp"></a>JET_SNP


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_snp"></a>JET_SNP

**JET_SNP** группа констант описывает тип операции, для которой необходимо получить сведения о ходе выполнения. Эти константы используются в качестве параметра *SNP* функции обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .


| <p>Константа/значение</p> | <p>Описание</p> | 
|-----------------------|--------------------|
| <p>JET_snpRepair<br />2</p> | <p>Обратный вызов предназначен для операции исправления.</p> | 
| <p>JET_snpCompact<br />4</p> | <p>Обратный вызов предназначен для дефрагментации базы данных.</p> | 
| <p>JET_snpRestore<br />8</p> | <p>Обратный вызов предназначен для операции восстановления.</p> | 
| <p>JET_snpBackup<br />9</p> | <p>Обратный вызов предназначен для операции резервного копирования.</p> | 
| <p>JET_snpUpgrade<br />10</p> | <p>Не поддерживается.</p><p><strong>Windows 2000:</strong>  Обратный вызов предназначен для операции обновления формата базы данных.</p> | 
| <p>JET_snpScrub<br />11</p> | <p>Обратный вызов предназначен для операции обнуления (т. е. очистки) базы данных.</p><p><strong>сервер Windows 2003 и Windows 2000:</strong>  Не поддерживается.</p> | 
| <p>JET_snpUpgradeRecordFormat<br />12</p> | <p>Обратный вызов предназначен для процесса обновления формата записей всех страниц базы данных.</p><p><strong>сервер Windows 2003 и Windows 2000:</strong>  Не поддерживается.</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
