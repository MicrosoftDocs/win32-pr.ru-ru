---
description: Разделы реестра могут быть записаны в системный реестр после установки всех выбранных компонентов и связанных с ними файлов.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Изменение реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348525"
---
# <a name="modifying-the-registry"></a><span data-ttu-id="3f021-103">Изменение реестра</span><span class="sxs-lookup"><span data-stu-id="3f021-103">Modifying the Registry</span></span>

<span data-ttu-id="3f021-104">Разделы реестра могут быть записаны в системный реестр после установки всех выбранных компонентов и связанных с ними файлов.</span><span class="sxs-lookup"><span data-stu-id="3f021-104">Registry keys can be written to the system registry once all selected components and their related files have been installed.</span></span> <span data-ttu-id="3f021-105">Стандартные действия, связанные с изменением реестра, должны быть упорядочены после стандартных действий установки файлов, так как разделы реестра не могут быть записаны, если только соответствующий компонент и файл не были успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="3f021-105">The standard actions related to modifying the registry must be sequenced after the file installation standard actions because registry keys cannot be written unless the corresponding component and file have been successfully installed.</span></span>

<span data-ttu-id="3f021-106">[Действие регистерклассинфо](registerclassinfo-action.md) обращается к [таблице классов](class-table.md) для регистрации сведений о COM-классе установленных компонентов.</span><span class="sxs-lookup"><span data-stu-id="3f021-106">The [RegisterClassInfo action](registerclassinfo-action.md) accesses the [Class table](class-table.md) to register the COM class information of the installed components.</span></span>

<span data-ttu-id="3f021-107">[Действие регистерекстенсионинфо](registerextensioninfo-action.md) запрашивает [таблицу расширения](extension-table.md) и [таблицу команд](verb-table.md) и регистрирует соответствующие расширения и сведения о командных командах в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="3f021-107">The [RegisterExtensionInfo action](registerextensioninfo-action.md) queries the [Extension table](extension-table.md) and [Verb table](verb-table.md) and registers the corresponding extensions and command-verb information with the operating system.</span></span>

<span data-ttu-id="3f021-108">[Действие регистерпрогидинфо](registerprogidinfo-action.md) управляет регистрацией данных OLE ProgID в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="3f021-108">The [RegisterProgIdInfo action](registerprogidinfo-action.md) manages the registration of OLE ProgId information with the operating system.</span></span>

<span data-ttu-id="3f021-109">[Действие регистермимеинфо](registermimeinfo-action.md) обрабатывает [таблицу MIME](mime-table.md) для регистрации связи между типом контекста MIME, расширением имени файла и идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="3f021-109">The [RegisterMIMEInfo action](registermimeinfo-action.md) processes the [MIME table](mime-table.md) to register the association between a MIME context type, the file name extension, and the CLSID.</span></span>

<span data-ttu-id="3f021-110">[Действие вритерегистривалуес](writeregistryvalues-action.md) обрабатывает [таблицу реестра](registry-table.md) и записывает ключи для всех компонентов, которые были либо установлены локально, либо для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="3f021-110">The [WriteRegistryValues action](writeregistryvalues-action.md) processes the [Registry table](registry-table.md) and writes the keys for all components that have been either installed locally or to run from source.</span></span> <span data-ttu-id="3f021-111">Таблица реестра позволяет записывать ключи в **\_ \_ корневую папку классов hKey**, раздел **hKey \_ текущий \_ пользователь**, **hKey \_ локальный \_ компьютер** и куст реестра **hKey пользователя \_** .</span><span class="sxs-lookup"><span data-stu-id="3f021-111">The Registry table allows keys to be written to the **HKEY\_CLASSES\_ROOT**, **HKEY\_CURRENT\_USER**, **HKEY\_LOCAL\_MACHINE**, and **HKEY\_USERS** registry hives.</span></span>

<span data-ttu-id="3f021-112">[Действие ремоверегистривалуес](removeregistryvalues-action.md) удаляет ключи, которые были помечены для удаления в столбце имя [таблицы реестра](registry-table.md) или [таблицы ремоверегистри](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f021-112">The [RemoveRegistryValues action](removeregistryvalues-action.md) removes the keys that have been marked to be deleted in the Name column of the [Registry table](registry-table.md) or the [RemoveRegistry Table](removeregistry-table.md).</span></span>

<span data-ttu-id="3f021-113">[Действие регистертипелибрариес](registertypelibraries-action.md) обрабатывает [таблицу typelib](typelib-table.md) и регистрирует установленные библиотеки типов в системе.</span><span class="sxs-lookup"><span data-stu-id="3f021-113">The [RegisterTypeLibraries action](registertypelibraries-action.md) processes the [TypeLib table](typelib-table.md) and registers the installed type libraries with the system.</span></span>

 

 



