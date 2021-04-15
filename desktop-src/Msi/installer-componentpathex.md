---
description: Возвращает объект Рекордлист, предоставляющий полный путь к указанному установленному компоненту.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Свойство Installer. Компонентпасекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651965"
---
# <a name="installercomponentpathex-property"></a>Свойство Installer. Компонентпасекс

Это свойство возвращает объект [**рекордлист**](recordlist-object.md) , который предоставляет полный путь к указанному установленному компоненту. Это свойство вызывает [**мсижеткомпонентпасекс**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).

**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается. Это свойство доступно, начиная с установщик Windows 5,0.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсижеткомпонентпасекс**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




