---
description: Свойство Патчесекс возвращает объект Рекордлист, перечисляющий список исправлений.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Свойство Installer. Патчесекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651659"
---
# <a name="installerpatchesex-property"></a>Свойство Installer. Патчесекс

Свойство **патчесекс** возвращает объект [**рекордлист**](recordlist-object.md) , перечисляющий список исправлений. Это свойство вызывает [**мсиенумпатчесекс**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Установщик**](installer-object.md)
</dt> <dt>

[**мсиенумпатчесекс**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**Защиты**](patch-object.md)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




