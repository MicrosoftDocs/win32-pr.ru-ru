---
description: Метод Конфигурефеатуре объекта Installer настраивает установленное состояние компонента продукта.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configметод Урефеатуре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 522dfffcbafd546dce218956729f01133708833a4a4c2732af3ea0248f87bc71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632350"
---
# <a name="installerconfigurefeature-method"></a>Installer.Configметод Урефеатуре

Метод **конфигурефеатуре** объекта [**Installer**](installer-object.md) настраивает установленное состояние компонента продукта.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Продукт* 
</dt> <dd>

Указывает код продукта.

</dd> <dt>

*Компонент* 
</dt> <dd>

Указывает идентификатор компонента для настраиваемого компонента.

</dd> <dt>

*InstallState* 
</dt> <dd>

Указывает состояние установки для компонента. Этот параметр должен иметь одно из следующих значений.



| Значение                                                                                                                                                                                                                                        | Значение                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**мсиинсталлстатеадвертисед**</dt> </dl> | Эта функция объявлена<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**мсиинсталлстателокал**</dt> </dl>                     | Этот компонент устанавливается локально.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**мсиинсталлстатеабсент**</dt> </dl>                 | Компонент удален.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**мсиинсталлстатесаурце**</dt> </dl>                 | Компонент устанавливается для запуска из источника.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**мсиинсталлстатедефаулт**</dt> </dl>             | Компонент устанавливается в расположение по умолчанию.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[Функции установки и настройки](installer-function-reference.md)
</dt> </dl>

 

 




