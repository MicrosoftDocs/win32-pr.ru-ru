---
description: Свойство Продуктелеватед объекта Installer возвращает значение true, если продукт является управляемым, или значение false, если продукт не является управляемым.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Установщик::P свойство Родуктелеватед
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 515964481c62e4588f3d9b75d168bffd2876cb22ce526e8ec0eaa41e226c110e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129394"
---
# <a name="installerproductelevated-property"></a>Установщик::P свойство Родуктелеватед

Свойство **продуктелеватед** объекта [**Installer**](installer-object.md) возвращает значение true, если продукт является управляемым, или значение false, если продукт не является управляемым.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Значение свойства

Полный идентификатор GUID кода продукта. Это обязательный параметр.

## <a name="remarks"></a>Remarks

Свойство **продуктелеватед** использует функцию [**мсииспродуктелеватед**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) . Возврат свойства не учитывает политику [AlwaysInstallElevated](alwaysinstallelevated.md) .

## <a name="examples"></a>Примеры

В следующем примере скрипта демонстрируется использование свойства **продуктелеватед** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 4,5 на Windows Server 2003 и Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Установщик**](installer-object.md)
</dt> <dt>

[не поддерживается в установщик Windows 3,1 и более ранних версиях](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




