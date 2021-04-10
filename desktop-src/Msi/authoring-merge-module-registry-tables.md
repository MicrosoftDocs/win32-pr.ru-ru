---
description: Используйте таблицы реестра модуля слияния в соответствии с типом данных реестра.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Создание таблиц реестра для модуля слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998275"
---
# <a name="authoring-merge-module-registry-tables"></a><span data-ttu-id="ec4a0-103">Создание таблиц реестра для модуля слияния</span><span class="sxs-lookup"><span data-stu-id="ec4a0-103">Authoring Merge Module Registry Tables</span></span>

<span data-ttu-id="ec4a0-104">Используйте таблицы реестра модуля слияния в соответствии с типом данных реестра.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-104">Use Merge Module Registry tables according to the type of registry information.</span></span>

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a><span data-ttu-id="ec4a0-105">TypeLib, Class, AppId, ProgId, расширение, глагол или таблицы MIME</span><span class="sxs-lookup"><span data-stu-id="ec4a0-105">TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME Tables</span></span>

<span data-ttu-id="ec4a0-106">Для библиотек типов, классов, расширений и команд создайте сведения о реестре в [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [расширении](extension-table.md), [глаголе](verb-table.md)или таблицах [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="ec4a0-106">For type libraries, classes, extensions, and verbs, author registry information into the merge module's [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="ec4a0-107">Если вы используете [таблицу реестра](registry-table.md) для добавления этих сведений, Windows 2000 не может предоставить объявления для этих компонентов в масштабе всей системы.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-107">If you use the [Registry table](registry-table.md) to add this information, Windows 2000 cannot provide system-wide advertisement for these components.</span></span>

<span data-ttu-id="ec4a0-108">Авторы модулей слияния могут решить не выполнять регистрацию с помощью таблицы классов по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="ec4a0-108">Merge module authors may decide not to register using the Class table for the following reasons:</span></span>

-   <span data-ttu-id="ec4a0-109">Для регистрации в таблице классов файл должен быть ключевой точкой его компонента.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-109">To be registered by the Class table, the file has to be the KeyPath of its component.</span></span> <span data-ttu-id="ec4a0-110">Это может потребовать неприемлемого изменения в организации компонентов.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-110">This may require an unacceptable change in the organization of components.</span></span>
-   <span data-ttu-id="ec4a0-111">Вызов COM может вызвать попытку установщика переустановить объявленный класс.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-111">A COM call may trigger an installer attempt to reinstall an advertised class.</span></span> <span data-ttu-id="ec4a0-112">Авторы могут решить не регистрировать класс с помощью таблицы классов, чтобы избежать повторной установки, если клиентский компьютер не поддерживает пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-112">Authors may decide not to register a class using the Class table in order to avoid triggering a reinstallation when the client computer does not support a user interface.</span></span>

## <a name="registry-table"></a><span data-ttu-id="ec4a0-113">Таблица реестра</span><span class="sxs-lookup"><span data-stu-id="ec4a0-113">Registry Table</span></span>

<span data-ttu-id="ec4a0-114">Используйте таблицу реестра для добавления данных реестра, которые не могут быть созданы в TypeLib, Class, AppId, ProgId, расширении, глаголе или таблицах MIME.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-114">Use the Registry table to add registry information that cannot be authored into the TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME tables.</span></span> <span data-ttu-id="ec4a0-115">Windows 2000 не может предоставить системное объявление для компонентов, использующих таблицу реестра.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-115">Windows 2000 cannot provide system-wide advertisement for components that use the Registry table.</span></span>

<span data-ttu-id="ec4a0-116">При создании таблицы реестра ознакомьтесь с путями к файлам с помощью \[ \# файла \] или \[ ! \]Формат файла, а не \[ \] имя файла каталога.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-116">When authoring the Registry table, refer to file paths using the \[\#File\] or \[!File\] format rather than as \[Directory\]Filename.</span></span> <span data-ttu-id="ec4a0-117">Последний формат не поддерживает установку с запуском с исходного кода.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-117">The latter format does not support run-from-source installation.</span></span> <span data-ttu-id="ec4a0-118">Первый формат также упрощает обнаружение отсутствующих файлов и неисправных компонентов.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-118">The former format also makes missing files and faulty components easier to detect.</span></span>

<span data-ttu-id="ec4a0-119">При использовании форматированного текста в ключевом столбце таблицы реестра необходимо соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-119">Care is needed when using formatted text in the Key column of the Registry table.</span></span> <span data-ttu-id="ec4a0-120">Поскольку установщик Windows не переустанавливает уже установленные компоненты, использование форматированного текста в этом поле может привести к тому, что разделы реестра будут оставлены после удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-120">Because Windows Installer does not reinstall components that are already installed, using formatted text in this field may cause registry keys to be left behind on application removal.</span></span>

## <a name="selfreg-table"></a><span data-ttu-id="ec4a0-121">Таблица Селфрег</span><span class="sxs-lookup"><span data-stu-id="ec4a0-121">SelfReg Table</span></span>

<span data-ttu-id="ec4a0-122">Использовать таблицу Селфрег не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-122">Using the SelfReg table is not recommended.</span></span> <span data-ttu-id="ec4a0-123">Список причин, по которым не используется самостоятельная регистрация, см. в разделе [селфрег Table](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="ec4a0-123">For a list of reasons for not using self-registration, see [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="ec4a0-124">Вместо этого следует использовать таблицы TypeLib, Class, AppId, ProgId, расширение, глагол и MIME, где это возможно, а также таблица реестра во всех остальных случаях.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-124">You should use the TypeLib, Class, AppId, ProgId, Extension, Verb, and MIME tables where possible instead and the Registry table in all other cases.</span></span>

 

 



