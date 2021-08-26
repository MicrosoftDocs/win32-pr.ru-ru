---
description: список свойств установщик Windows, предоставляя значения, записанные в разделе реестра Uninstall.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Свойства установщика для раздела реестра Uninstall
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: b898cd2a83a05783141ddf1fb4a7cbebb783bbcd7640526c5b653afa434d2175
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810323"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Свойства установщика для раздела реестра Uninstall

Следующие свойства установщика предоставляют значения, записываемые в раздел реестра:

**HKey \_ \_** \\ **программное обеспечение** локального компьютера ( \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\  )

Значения хранятся в подразделе, определяемом идентификатором GUID кода продукта приложения.



| Значение               | Windows Свойство установщика                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | Свойство [**ProductName**](productname.md)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Производный от свойства [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Издатель           | Свойство [**Manufacturer**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Производный от свойства [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Производный от свойства [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Версия             | Производный от свойства [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | [**Арфелплинк**](arphelplink.md) , свойство                                                                                                                                                                                                                                                                                                                          |
| хелптелефоне       | [**Арфелптелефоне**](arphelptelephone.md) , свойство                                                                                                                                                                                                                                                                                                                |
| InstallDate         | Время последнего поступления этого продукта в службу. Значение этого свойства заменяется каждый раз, когда к продукту применяется или удаляется исправление, или для восстановления продукта используется [параметр командной строки](command-line-options.md) /v. Если продукт не получил исправлений или обновлений, это свойство содержит время установки продукта на этом компьютере. |
| InstallLocation     | [**Арпинсталллокатион**](arpinstalllocation.md) , свойство                                                                                                                                                                                                                                                                                                            |
| инсталлсаурце       | [**SourceDir**](sourcedir.md) , свойство                                                                                                                                                                                                                                                                                                                              |
| урлинфоабаут        | [**Арпурлинфоабаут**](arpurlinfoabout.md) , свойство                                                                                                                                                                                                                                                                                                                  |
| урлупдатеинфо       | [**Арпурлупдатеинфо**](arpurlupdateinfo.md) , свойство                                                                                                                                                                                                                                                                                                                |
| аусоризедкдфпрефикс | [**Арпаусоризедкдфпрефикс**](arpauthorizedcdfprefix.md) , свойство                                                                                                                                                                                                                                                                                                    |
| Примечания            | [**Арпкомментс**](arpcomments.md) , свойство <br/> Комментарии, указанные на панели управления " **Установка и удаление программ** ".<br/>                                                                                                                                                                                                                                |
| Contact             | [**Арпконтакт**](arpcontact.md) , свойство <br/> Обратитесь к панели управления **Установка и удаление программ** .<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | определяется и задается установщик Windows.                                                                                                                                                                                                                                                                                                                         |
| Язык            | [**Продуктлангуаже**](productlanguage.md) , свойство                                                                                                                                                                                                                                                                                                                  |
| модифипас          | определяется и задается установщик Windows.                                                                                                                                                                                                                                                                                                                         |
| Readme              | [**Арпреадме**](arpreadme.md) , свойство <br/> Файл readme, указанный на панели управления " **Установка и удаление программ** ".<br/>                                                                                                                                                                                                                                      |
| UninstallString     | определяется и задается установщик Windows.                                                                                                                                                                                                                                                                                                                             |
| сеттингсидентифиер  | [**Мсиарпсеттингсидентифиер**](msiarpsettingsidentifier.md) , свойство                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения о свойствах](about-properties.md)
</dt> <dt>

[настройка установки и удаления программ с помощью установщик Windows](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Справочник по свойствам](property-reference.md)
</dt> <dt>

[Использование свойств](using-properties.md)
</dt> </dl>

 

 




