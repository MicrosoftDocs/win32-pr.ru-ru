---
description: сведения о установщик Windows концепциях, начинающихся с буквы P, например кода пакета и исправлений.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74af2780852bcb59124390042bfdbbc7bf2e7618cdb4167f58b15fc04ab1b15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942764"
---
# <a name="p-windows-installer"></a>P (установщик Windows)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**пакеты**
</dt> <dd>

[*Файл.msi*](m-gly.md) и все [*Внешние исходные файлы*](e-gly.md) , на которые может указывать этот файл. таким образом, пакет содержит все сведения, необходимые установщик Windows для запуска пользовательского интерфейса и установки или удаления приложения. Дополнительные сведения см. в разделе также [*база данных установщика*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**код пакета**
</dt> <dd>

Идентификатор GUID, определяющий конкретный пакет. Уникальный код пакета является обязательным, так как некоторые преобразования или пакеты исправлений могут применяться к нескольким приложениям или могут обновить приложение в другом приложении или версии. Дополнительные сведения см. в разделе [коды пакетов](package-codes.md).

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**исправления**
</dt> <dd>

Метод обновления файла, который заменяет только изменяемые биты, а не весь файл. Это означает, что пользователи могут загрузить обновление для продукта, который намного меньше, чем весь продукт. Дополнительные сведения см. в разделе [пакеты исправлений](patch-packages.md).

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**файл исправления**
</dt> <dd>

[Пакет P атч](patch-packages.md) , используемый для установки исправлений. Дополнительные сведения см. в разделе [Установка исправлений и обновления](patching-and-upgrades.md).

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**режим предварительного просмотра**
</dt> <dd>

Режим для просмотра макета пользовательского интерфейса. Дополнительные сведения см. [в разделе Предварительный просмотр пользовательского интерфейса](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**индикатор выполнения**
</dt> <dd>

Управление, которое может отображаться установщиком во время выполнения сценария, представляющее ход установки. Дополнительные сведения см. [в разделе Authoring a ProgressBar Control](authoring-a-progressbar-control.md).

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**свойства**
</dt> <dd>

Глобальные переменные, используемые во время установки. (См. раздел [о свойствах](about-properties.md).)

Термин "свойство" также ссылается на атрибут объекта автоматизации. (См. раздел [интерфейс автоматизации](automation-interface.md).)

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Publish**
</dt> <dd>

Метод [*объявления*](a-gly.md) функции или приложения. Публикация не заполняет пользовательский интерфейс. Однако, если другое приложение пытается открыть опубликованное приложение, установщику будет назначено достаточно информации для назначения опубликованного приложения. Дополнительные сведения см. в разделе [*назначение*](a-gly.md) и [компоненты](components-and-features.md)и компоненты.

</dd> </dl>

 

 



