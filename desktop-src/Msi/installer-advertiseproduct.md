---
description: Метод Адвертисепродукт объекта Installer объявляет пакет установки.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Метод Installer:: Адвертисепродукт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651915"
---
# <a name="installeradvertiseproduct-method"></a>Метод Installer:: Адвертисепродукт

Метод **адвертисепродукт** объекта [**Installer**](installer-object.md) объявляет пакет установки.

## <a name="syntax"></a>Синтаксис


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*packagePath* 
</dt> <dd>

Полный путь к пакету установщик Windows (MSI), который требуется объявить.

</dd> <dt>

*context* 
</dt> <dd>

Контекст объявления. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                                                                   | Значение                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**мсиадвертисепродуктмачине**</dt> <dt>0</dt> </dl> | Объявляет приложение для [установки в контексте инсталляции](installation-context.md)для каждого компьютера. Это сделает пакет доступным для установки всеми пользователями компьютера.<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**мсиадвертисепродуктусер**</dt> <dt>1</dt> </dl>             | Объявляет приложение для установки в [контексте установки](installation-context.md)на уровне пользователя.<br/>                                                                                   |



 

</dd> <dt>

*преобразования* 
</dt> <dd>

Список преобразований, применяемых к продукту. Преобразования в списке разделяются точками с запятой. Это необязательный параметр.

</dd> <dt>

*language* 
</dt> <dd>

Язык используемого пакета установки. Это необязательный параметр.

</dd> <dt>

*options* 
</dt> <dd>

Параметры объявления. Это необязательный параметр. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                                                                   | Значение                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**мсиадвертиседефаулт**</dt> <dt>0</dt> </dl>                             | Стандартное объявление<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**мсиадвертисесинглеинстанце**</dt> <dt>1</dt> </dl> | Объявляет новый экземпляр продукта. Требует, чтобы первое преобразование в списке *преобразования параметра* преобразований было преобразованием экземпляра, которое изменяет код продукта. Дополнительные сведения см. в разделе [Установка нескольких экземпляров продуктов и исправлений](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Метод **адвертисепродукт** использует функцию [**мсиадвертисепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование метода **адвертисепродукт** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
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

 

 




