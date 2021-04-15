---
description: Свойство SummaryInformation объекта Installer возвращает объект Суммаринфо, который может использоваться для проверки, обновления и добавления свойств в поток сводных данных пакета или преобразования.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Свойство Installer. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651658"
---
# <a name="installersummaryinformation-property"></a>Свойство Installer. SummaryInformation

Свойство **SummaryInformation** объекта [**Installer**](installer-object.md) возвращает объект [**суммаринфо**](summaryinfo-object.md) , который может использоваться для проверки, обновления и добавления свойств в поток сводных данных пакета или преобразования.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Комментарии

Если для открытия существующего потока сводных данных используется значение *макспропертиес* больше 0, то перед закрытием объекта необходимо вызвать метод [**Persist**](summaryinfo-persist.md) . В противном случае существующие данные о потоке будут утеряны.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




