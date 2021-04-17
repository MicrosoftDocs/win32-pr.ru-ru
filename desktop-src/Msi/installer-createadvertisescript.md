---
description: Метод Креатеадвертисескрипт объекта Installer создает скрипт объявления.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Метод Installer:: Креатеадвертисескрипт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652288"
---
# <a name="installercreateadvertisescript-method"></a>Метод Installer:: Креатеадвертисескрипт

Метод **креатеадвертисескрипт** объекта [**Installer**](installer-object.md) создает скрипт объявления.

## <a name="syntax"></a>Синтаксис


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*packagePath* 
</dt> <dd>

Полный путь к пакету установщик Windows (MSI), который требуется объявить.

</dd> <dt>

*скриптфилепас* 
</dt> <dd>

Полный путь к файлу скрипта, который создается с объявленной информацией.

</dd> <dt>

*преобразования* 
</dt> <dd>

Список преобразований, применяемых к продукту. Преобразования в списке разделяются точками с запятой. Это необязательный параметр.

</dd> <dt>

*language* 
</dt> <dd>

Язык используемого пакета установки. Это необязательный параметр.

</dd> <dt>

*platform* 
</dt> <dd>

Этот параметр указывает, для какой платформы установщик должен создать скрипт. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                                                                       | Значение                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <dt>**мсиадвертисекуррентплатформ**</dt> <dt>0</dt> </dl> | Создает скрипт для текущей платформы.<br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt> </dl>                 | Создает скрипт для платформы x86.<br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt> </dl>             | Создает скрипт для систем на базе процессоров Itanium.<br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt> </dl>                 | Создает скрипт для платформы x64.<br/>      |



 

</dd> <dt>

*options* 
</dt> <dd>

Параметры объявления. Это необязательный параметр. Этот параметр может принимать одно из указанных ниже значений. Это необязательный параметр.



| Значение                                                                                                                                                                                                                                                                                                   | Значение                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**мсиадвертиседефаулт**</dt> <dt>0</dt> </dl>                             | Стандартное объявление<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**мсиадвертисесинглеинстанце**</dt> <dt>1</dt> </dl> | Объявляет новый экземпляр продукта. Требует, чтобы первое преобразование в списке *преобразования параметра* преобразований было преобразованием экземпляра, которое изменяет код продукта. Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Метод [**адвертисепродукт**](installer-advertiseproduct.md) использует функцию [**мсиадвертисепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование метода **креатеадвертисескрипт** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
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

 

 




