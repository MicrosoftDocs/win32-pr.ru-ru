---
description: Свойство Продуктинфофромскрипт объекта Installer возвращает значение указанного атрибута, хранящегося в скрипте объявления.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Установщик::P свойство Родуктинфофромскрипт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652224"
---
# <a name="installerproductinfofromscript-property"></a>Установщик::P свойство Родуктинфофромскрипт

Свойство **продуктинфофромскрипт** объекта [**Installer**](installer-object.md) возвращает значение указанного атрибута, хранящегося в скрипте объявления.

Это свойство доступно только на запись.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a>Значение свойства

## <a name="error-codes"></a>Коды ошибок

Строковое или целочисленное значение, зависящее от запрошенного атрибута.

## <a name="remarks"></a>Комментарии

Свойство **продуктинфофромскрипт** использует функцию [**мсижетпродуктинфофромскрипт**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) .

## <a name="examples"></a>Примеры

В следующем примере скрипта демонстрируется использование свойства **продуктинфофромскрипт** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 4,5 в Windows Server 2003 и Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Установщик**](installer-object.md)
</dt> <dt>

[Не поддерживается в установщик Windows 3,1 и более ранних версиях](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




