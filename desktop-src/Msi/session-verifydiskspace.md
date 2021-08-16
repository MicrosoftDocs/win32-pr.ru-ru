---
description: Свойство Верифидискспаце доступно только для чтения.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Свойство Session. Верифидискспаце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4a50bb96088f2c52673fda9a9ddffd786657376bcb4e4a60d5c6d81cb4fbe5e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628764"
---
# <a name="sessionverifydiskspace-property"></a>Свойство Session. Верифидискспаце

Свойство **верифидискспаце** доступно только для чтения. Он возвращает значение true, если существует достаточно места на диске, и значение false, если диск заполнен. Поскольку это свойство использует сведения, собранные действиями по затратам, **верифидискспаце** следует вызывать только после действия [костинитиализе](costinitialize-action.md), [филекост Action](filecost-action.md)и [костфинализе](costfinalize-action.md).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




