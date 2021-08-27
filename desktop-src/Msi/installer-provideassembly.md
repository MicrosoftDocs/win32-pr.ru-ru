---
description: Метод Провидеассембли объекта Installer возвращает установленный путь к сборке.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Установщик::P метод Ровидеассембли
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 45d5c2d6b64936b034d859caddf72ddaaf6fba77451d066205d7f394200311f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105214"
---
# <a name="installerprovideassembly-method"></a>Установщик::P метод Ровидеассембли

Метод **провидеассембли** объекта [**Installer**](installer-object.md) возвращает установленный путь к сборке.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сборок* 
</dt> <dd>

Строгое имя установленной сборки, к которой выполняется запрос.

</dd> <dt>

*appContext* 
</dt> <dd>

Задайте для глобальных сборок значение null. Для закрытых сборок задайте для *appContext* полный путь к файлу конфигурации приложения или полный путь к исполняемому файлу приложения, для которого сборка была закрыта.

</dd> <dt>

*installMode* 
</dt> <dd>

Определяет режим установки. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                                                                                                                                              | Значение                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**мсиинсталлмодедефаулт**</dt> <dt>0</dt> </dl>                                                                                                | Укажите компонент и выполните установку, необходимую для предоставления компонента. <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**мсиинсталлмодиксистинг**</dt> <dt>-1</dt> </dl>                                                                                           | Предоставьте компонент только в том случае, если компонент существует. Этот параметр позволяет проверить существование сборки.<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**мсиинсталлмоденодетектион**</dt> <dt>-2</dt> </dl>                                                                               | Предоставьте компонент только в том случае, если компонент существует. Этот параметр не проверяет существование сборки.<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**мсиинсталлмоденосаурцересолутион**</dt> <dt>-3</dt> </dl>                                                   | Предоставляет сборку только в том случае, если сборка установлена локально.<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**Сочетание флагов, используемых [ **реинсталлфеатуре**](installer-reinstallfeature.md)**</dt> </dl> | Вызывает метод [**реинсталлфеатуре**](installer-reinstallfeature.md) для переустановки компонента с помощью этого параметра для *ReinstallMode*, а затем возвращает путь к сборке.<br/> |



 

</dd> <dt>

*Файле* 
</dt> <dd>

Сведения о сборке и тип сборки. Задайте одно из следующих значений.



| Значение                                                                                                                                                                                                                                                                                       | Значение                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**мсипровидеассемблинет**</dt> <dt>0</dt> </dl>         | Сборка .NET.<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Параллельная сборка Win32.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Путь к установленной сборке.

## <a name="remarks"></a>Remarks

Метод **провидеассембли** использует функцию [**мсипровидеассембли**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .

## <a name="examples"></a>Примеры

В следующем примере сценария демонстрируется использование метода Провидеассембли.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a>Requirements (Требования)



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

 

 




