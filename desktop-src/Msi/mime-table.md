---
description: Таблица MIME связывает MIME-тип содержимого с расширением имени файла или идентификатором CLSID, чтобы создать сведения о расширении или сервере COM, необходимые для объявления содержимого MIME (многоцелевые расширения электронной почты Интернета).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Таблица MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265825"
---
# <a name="mime-table"></a><span data-ttu-id="837ab-103">Таблица MIME</span><span class="sxs-lookup"><span data-stu-id="837ab-103">MIME Table</span></span>

<span data-ttu-id="837ab-104">Таблица MIME связывает MIME-тип содержимого с расширением имени файла или идентификатором CLSID, чтобы создать сведения о расширении или сервере COM, необходимые для объявления содержимого MIME (многоцелевые расширения электронной почты Интернета).</span><span class="sxs-lookup"><span data-stu-id="837ab-104">The MIME table associates a MIME content type with a file name extension or a CLSID to generate the extension or COM server information required for advertisement of the MIME (Multipurpose Internet Mail Extensions) content.</span></span>

<span data-ttu-id="837ab-105">Таблица MIME содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="837ab-105">The MIME table has the following columns.</span></span>



| <span data-ttu-id="837ab-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="837ab-106">Column</span></span>      | <span data-ttu-id="837ab-107">Type</span><span class="sxs-lookup"><span data-stu-id="837ab-107">Type</span></span>             | <span data-ttu-id="837ab-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="837ab-108">Key</span></span> | <span data-ttu-id="837ab-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="837ab-109">Nullable</span></span> |
|-------------|------------------|-----|----------|
| <span data-ttu-id="837ab-110">ContentType</span><span class="sxs-lookup"><span data-stu-id="837ab-110">ContentType</span></span> | [<span data-ttu-id="837ab-111">Text</span><span class="sxs-lookup"><span data-stu-id="837ab-111">Text</span></span>](text.md) | <span data-ttu-id="837ab-112">Да</span><span class="sxs-lookup"><span data-stu-id="837ab-112">Y</span></span>   | <span data-ttu-id="837ab-113">Нет</span><span class="sxs-lookup"><span data-stu-id="837ab-113">N</span></span>        |
| <span data-ttu-id="837ab-114">Расширение\_</span><span class="sxs-lookup"><span data-stu-id="837ab-114">Extension\_</span></span> | [<span data-ttu-id="837ab-115">Text</span><span class="sxs-lookup"><span data-stu-id="837ab-115">Text</span></span>](text.md) | <span data-ttu-id="837ab-116">Нет</span><span class="sxs-lookup"><span data-stu-id="837ab-116">N</span></span>   | <span data-ttu-id="837ab-117">Нет</span><span class="sxs-lookup"><span data-stu-id="837ab-117">N</span></span>        |
| <span data-ttu-id="837ab-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="837ab-118">CLSID</span></span>       | [<span data-ttu-id="837ab-119">GUID</span><span class="sxs-lookup"><span data-stu-id="837ab-119">GUID</span></span>](guid.md) | <span data-ttu-id="837ab-120">Нет</span><span class="sxs-lookup"><span data-stu-id="837ab-120">N</span></span>   | <span data-ttu-id="837ab-121">Да</span><span class="sxs-lookup"><span data-stu-id="837ab-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="837ab-122">Столбцы</span><span class="sxs-lookup"><span data-stu-id="837ab-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="837ab-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span><span class="sxs-lookup"><span data-stu-id="837ab-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span></span>
</dt> <dd>

<span data-ttu-id="837ab-124">Этот столбец является идентификатором MIME-содержимого.</span><span class="sxs-lookup"><span data-stu-id="837ab-124">This column is an identifier for the MIME content.</span></span> <span data-ttu-id="837ab-125">Обычно он написан в формате типа/Format.</span><span class="sxs-lookup"><span data-stu-id="837ab-125">It is commonly written in the form of type/format.</span></span>

</dd> <dt>

<span data-ttu-id="837ab-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Продлен\_</span><span class="sxs-lookup"><span data-stu-id="837ab-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="837ab-127">Этот столбец содержит серверное расширение, которое должно быть связано с содержимым MIME, без точки.</span><span class="sxs-lookup"><span data-stu-id="837ab-127">This column contains the server extension that is to be associated with the MIME content, without the dot.</span></span> <span data-ttu-id="837ab-128">Этот столбец является внешним ключом в [таблице расширения](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="837ab-128">This column is a foreign key into the [Extension table](extension-table.md).</span></span> <span data-ttu-id="837ab-129">Таблица расширений содержит сведения о сервере расширения имени файла, которые используются как часть объявления.</span><span class="sxs-lookup"><span data-stu-id="837ab-129">The Extension table contains file name extension server information which is used as a part of advertisement.</span></span>

</dd> <dt>

<span data-ttu-id="837ab-130"><span id="CLSID"></span><span id="clsid"></span>ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="837ab-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="837ab-131">Этот столбец содержит CLSID COM-сервера, который должен быть связан с содержимым MIME.</span><span class="sxs-lookup"><span data-stu-id="837ab-131">This column contains the COM server CLSID that is to be associated with the MIME content.</span></span> <span data-ttu-id="837ab-132">Идентификатор CLSID в этом столбце может быть внешним ключом в [таблице классов](class-table.md) или идентификатором CLSID, который уже существует на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="837ab-132">The CLSID in this column can be a foreign key into the [Class table](class-table.md) or it can be a CLSID that already exists on the user's machine.</span></span> <span data-ttu-id="837ab-133">Таблица классов содержит сведения, относящиеся к серверу COM, которые используются как часть объявления.</span><span class="sxs-lookup"><span data-stu-id="837ab-133">The Class table contains COM server-related information which is used as a part of advertisement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="837ab-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="837ab-134">Remarks</span></span>

<span data-ttu-id="837ab-135">Эта таблица упоминается при выполнении [действия регистермимеинфо](registermimeinfo-action.md) или [унрегистермимеинфо](unregistermimeinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="837ab-135">This table is referred to when the [RegisterMIMEInfo action](registermimeinfo-action.md) or the [UnregisterMIMEInfo action](unregistermimeinfo-action.md) is executed.</span></span> <span data-ttu-id="837ab-136">В режиме объявления действие Регистермимеинфо регистрирует все сведения MIME для серверов из таблицы MIME, для которой включена соответствующая функция.</span><span class="sxs-lookup"><span data-stu-id="837ab-136">In advertise mode, the RegisterMIMEInfo action registers all MIME information for servers from the MIME table for which the corresponding feature is enabled.</span></span> <span data-ttu-id="837ab-137">В противном случае действие регистрирует информацию MIME для серверов из таблицы MIME, для которой в данный момент выбрана соответствующая функция.</span><span class="sxs-lookup"><span data-stu-id="837ab-137">Otherwise the action registers MIME information for servers from the MIME table for which the corresponding feature is currently selected to be installed.</span></span> <span data-ttu-id="837ab-138">[Действие унрегистермимеинфо](unregistermimeinfo-action.md) отменяет регистрацию в системе сведений о реестре, связанных с MIME.</span><span class="sxs-lookup"><span data-stu-id="837ab-138">The [UnregisterMIMEInfo action](unregistermimeinfo-action.md) unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="837ab-139">Действие отменяет регистрацию сведений MIME для серверов из таблицы MIME, для которой в данный момент выбрана соответствующая функция для удаления.</span><span class="sxs-lookup"><span data-stu-id="837ab-139">The action unregisters MIME information for servers from the MIME table for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="validation"></a><span data-ttu-id="837ab-140">Проверка</span><span class="sxs-lookup"><span data-stu-id="837ab-140">Validation</span></span>

<dl>

[<span data-ttu-id="837ab-141">ICE03</span><span class="sxs-lookup"><span data-stu-id="837ab-141">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="837ab-142">ICE06</span><span class="sxs-lookup"><span data-stu-id="837ab-142">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="837ab-143">ICE15</span><span class="sxs-lookup"><span data-stu-id="837ab-143">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="837ab-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="837ab-144">ICE32</span></span>](ice32.md)  
</dl>

 

 



