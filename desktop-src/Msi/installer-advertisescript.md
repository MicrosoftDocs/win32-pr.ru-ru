---
description: Метод Адвертисескрипт объекта Installer объявляет пакет установки.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: 'Метод Installer:: Адвертисескрипт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6a3ca8b4c07b4bd19b9f5d5066ed17dcc5aa7edb5828741e32ee05197a83777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633221"
---
# <a name="installeradvertisescript-method"></a>Метод Installer:: Адвертисескрипт

Метод **адвертисескрипт** объекта [**Installer**](installer-object.md) объявляет пакет установки.

## <a name="syntax"></a>Синтаксис


```JScript
.AdvertiseScript(
  scriptPath,
  scriptFlags,
  removeItems
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*scriptPath* 
</dt> <dd>

Полный путь к файлу скрипта, созданному методом [**креатеадвертисескрипт**](installer-createadvertisescript.md) .

</dd> <dt>

*скриптфлагс* 
</dt> <dd>

Флаги, управляющие объявлением. Этот параметр может быть сочетанием следующих значений.



| Значение                                                                                                                                                                                                                                                                                                                                                                           | Значение                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt>**мсиадвертисескрипткачеинфо**</dt> <dt>0x001</dt> </dl>                                                                 | Включите этот флаг, если нужно создать или удалить значки.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt>**мсиадвертисескриптшорткутс**</dt> <dt>0x004</dt> </dl>                                                                 | Включите этот флаг, если нужно создать или удалить ярлыки.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt>**мсиадвертисескриптмачинеассигн**</dt> <dt>0x008</dt> </dl>                                                 | Включите этот флаг, если продукт должен быть назначен компьютеру.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt>**мсиадвертисескриптконфигуратионрегистратион**</dt> <dt>0x020</dt> </dl> | Включите этот флаг, если необходимо записать или удалить сведения о конфигурации и управлении в данных реестра.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt>**мсиадвертисескриптвалидатетрансформлист**</dt> <dt>0x040</dt> </dl>                 | Включите этот флаг, чтобы принудительно выполнить проверку преобразований, перечисленных в сценарии, по сравнению с ранее зарегистрированными преобразованиями для этого продукта. Обратите внимание, что конфликты преобразования обнаруживаются с помощью сравнения строк без учета регистра и оцениваются между установками для каждого пользователя и компьютера во всех [контекстах установки](installation-context.md).<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt>**мсиадвертисескриптклассинфорегистратион**</dt> <dt>0x080</dt> </dl>                 | Включите этот флаг, если необходимо записать или удалить сведения о объявлении в реестре, связанном с COM-классами.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt>**мсиадвертисескриптекстенсионинфорегистратион**</dt> <dt>0x100</dt> </dl> | Включите этот флаг, если необходимо записать или удалить сведения об объявлении в реестре, связанном с расширением.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt>**мсиадвертисескриптаппинфо**</dt> <dt>0x180</dt> </dl>                                                                         | Включите этот флаг, если необходимо записать или удалить сведения об объявлении в реестре.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt>**мсиадвертисескриптрегдата**</dt> <dt>0x1A0</dt> </dl>                                                                         | Включите этот флаг, если необходимо записать или удалить сведения об объявлении в реестре.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*ремовеитемс* 
</dt> <dd>

Значение TRUE, если указанные элементы должны быть удалены, а не созданы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод **адвертисескрипт** использует функцию [**мсиадвертисескрипт**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) . Использование метода **адвертисескрипт** требует, чтобы сценарий выполнялся в локальном системном процессе.

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование метода **адвертисескрипт** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' Advertise Simple package using an advertise script
'   created by CreateAdvertiseScript Method
'
'  Flags 424 indicate msiAdvertiseScriptMachineAssign, msiAdvertiseScriptRegData

Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, false

' Verify Simple is installed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")

'
' Remove Simple using advertise script
'
Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, true

' Verify simple is removed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 4,5 на Windows Server 2003 и Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Установщик**](installer-object.md)
</dt> <dt>

[не поддерживается в установщик Windows 3,1 и более ранних версиях](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




