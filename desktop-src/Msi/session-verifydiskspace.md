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
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679936"
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
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




