---
description: Свойство SummaryInformation объекта Database возвращает объект Суммаринфо, который может использоваться для проверки, обновления и добавления свойств в поток сводных данных.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Свойство Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652254"
---
# <a name="databasesummaryinformation-property"></a>Свойство Database. SummaryInformation

Свойство **SummaryInformation** объекта [**Database**](database-object.md) возвращает объект [**суммаринфо**](summaryinfo-object.md) , который может использоваться для проверки, обновления и добавления свойств в [поток сводных данных](summary-information-stream.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Значение свойства

Максимальное число добавляемых или изменяемых свойств. Этот параметр является обязательным и используется для выделения достаточной рабочей памяти во время создания потока. Хранение этого количества свойств не требуется. Значение, равное нулю, должно использоваться, если база данных открыта только для чтения, чтобы предотвратить обновление потока.

## <a name="remarks"></a>Комментарии

Если для открытия существующего потока сводных данных используется значение *макспропертиес* больше 0, то перед закрытием объекта необходимо вызвать метод [**Persist**](summaryinfo-persist.md) . В противном случае существующие сведения о потоке будут потеряны.

Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




