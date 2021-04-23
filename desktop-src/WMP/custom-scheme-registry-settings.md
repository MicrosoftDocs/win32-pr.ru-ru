---
title: Параметры реестра настраиваемой схемы
description: Параметры реестра настраиваемой схемы
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Проигрыватель Windows Media, параметры реестра пользовательских схем
- Проигрыватель Windows Media, схемы
- Проигрыватель Windows Media, реестр
- реестр, параметры настраиваемой схемы
- реестр, схемы
- реестр, параметры для проигрывателя Windows Media
- схемы
- параметры реестра настраиваемой схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067564"
---
# <a name="custom-scheme-registry-settings"></a><span data-ttu-id="d0721-111">Параметры реестра настраиваемой схемы</span><span class="sxs-lookup"><span data-stu-id="d0721-111">Custom Scheme Registry Settings</span></span>

<span data-ttu-id="d0721-112">Схемы — это пользовательские протоколы.</span><span class="sxs-lookup"><span data-stu-id="d0721-112">Schemes are custom protocols.</span></span> <span data-ttu-id="d0721-113">Проигрыватель Windows Media сохраняет список схем в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0721-113">Windows Media Player maintains a list of schemes in the registry on the user's computer.</span></span> <span data-ttu-id="d0721-114">Когда пользователь пытается воспроизвести файл цифрового мультимедиа, игрок сначала проверяет, поддерживает ли пакет SDK формат Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d0721-114">When the user attempts to play a digital media file, the Player first checks whether the Windows Media Format SDK supports the scheme.</span></span> <span data-ttu-id="d0721-115">Если это не так, проигрыватель проверяет схему на соответствие списку в реестре.</span><span class="sxs-lookup"><span data-stu-id="d0721-115">If it doesn't, the Player checks the scheme against the list in the registry.</span></span> <span data-ttu-id="d0721-116">Если совпадение найдено, проигрыватель проверяет значение, которое указывает, какая базовая технология или *Среда выполнения* (например, Microsoft DirectShow или пакет SDK Windows Media Format), можно использовать для воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="d0721-116">If a match is found, the Player then checks a value that indicates which underlying technology, or *runtime* (such as Microsoft DirectShow or the Windows Media Format SDK), can be used to play the file.</span></span> <span data-ttu-id="d0721-117">Если совпадений не найдено, проигрыватель предоставляет пользователю диалоговое окно с предупреждением, предлагающее пользователю получить разрешение на попытку воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="d0721-117">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="d0721-118">При потоковой передаче цифровых файлов мультимедиа с помощью настраиваемой схемы протокола можно предотвратить появление этого предупреждения на компьютере пользователя, зарегистрировав схему и указав значение для среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="d0721-118">If you stream digital media files using a custom protocol scheme, you can prevent this warning from appearing on the user's computer by registering the scheme and providing a value for the runtime.</span></span>

<span data-ttu-id="d0721-119">Список схем хранится в виде набора разделов реестра, соответствующих зарегистрированным схемам, без двоеточия и двух косых черт (://).</span><span class="sxs-lookup"><span data-stu-id="d0721-119">The list of schemes is maintained as a set of registry keys that match the registered schemes, without the colon and the two slashes (://).</span></span> <span data-ttu-id="d0721-120">Например, ключ для схемы wmhtml://, используемый для потоковой передачи мультимедиа с богатыми возможностями, называется "вмхтмл".</span><span class="sxs-lookup"><span data-stu-id="d0721-120">For example, the key for the wmhtml:// scheme, which is used to stream rich media, is named "wmhtml".</span></span> <span data-ttu-id="d0721-121">Отдельный список сохраняется для локального компьютера и для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0721-121">A separate list is maintained for the local machine and for each user.</span></span> <span data-ttu-id="d0721-122">Для локального компьютера ключи схемы являются подразделами следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="d0721-122">For the local machine, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="d0721-123">**HKEY \_ по на локальном \_ компьютере \\ программное обеспечение \\ Microsoft \\ мультимедиа \\ вмплайер \\ схемы\\**</span><span class="sxs-lookup"><span data-stu-id="d0721-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\**</span></span>

<span data-ttu-id="d0721-124">Например, ключ для схемы wmhtml://на локальном компьютере:</span><span class="sxs-lookup"><span data-stu-id="d0721-124">For example, the key for the wmhtml:// scheme for the local machine is:</span></span>

<span data-ttu-id="d0721-125">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ мультимедиа \\ вмплайер \\ схемы \\ вмхтмл**</span><span class="sxs-lookup"><span data-stu-id="d0721-125">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="d0721-126">Чтобы изменить значения в этом разделе или создать новый подраздел, текущий пользователь должен быть администратором компьютера.</span><span class="sxs-lookup"><span data-stu-id="d0721-126">To change values in this key or to create a new subkey, the current user must be an administrator for the computer.</span></span>

<span data-ttu-id="d0721-127">Для отдельных пользователей ключи схемы являются подразделами следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="d0721-127">For individual users, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="d0721-128">**HKEY \_ текущее \_ пользовательское \\ программное обеспечение \\ \\ \\ схемы проигрывателя Microsoft MediaPlayer \\\\**</span><span class="sxs-lookup"><span data-stu-id="d0721-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\**</span></span>

<span data-ttu-id="d0721-129">Например, ключ для схемы wmhtml://текущего пользователя:</span><span class="sxs-lookup"><span data-stu-id="d0721-129">For example, the key for the wmhtml:// scheme for the current user is:</span></span>

<span data-ttu-id="d0721-130">**HKEY \_ текущее \_ пользовательское \\ программное обеспечение \\ \\ \\ схемы проигрывателя Microsoft MediaPlayer \\ \\ вмхтмл**</span><span class="sxs-lookup"><span data-stu-id="d0721-130">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="d0721-131">При проверке зарегистрированных схем игрок сначала проверяет значения, расположенные на **\_ локальном \_ компьютере в hKey**.</span><span class="sxs-lookup"><span data-stu-id="d0721-131">When checking for registered schemes, the Player first checks the values located in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="d0721-132">Если для текущей схемы не найдено ни одного, игрок затем проверяет значения в поле **hKey \_ текущий \_ пользователь**.</span><span class="sxs-lookup"><span data-stu-id="d0721-132">If none are found for the current scheme, the Player next checks the values in **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="d0721-133">Если для текущей схемы не найдено ни одного, проигрыватель выводит предупреждение пользователю.</span><span class="sxs-lookup"><span data-stu-id="d0721-133">If none are found for the current scheme, the Player displays the warning to the user.</span></span>

<span data-ttu-id="d0721-134">Каждый подраздел схемы может содержать одно из следующих возможных значений для *среды выполнения*.</span><span class="sxs-lookup"><span data-stu-id="d0721-134">Each scheme subkey may contain one of the following possible values for *Runtime*.</span></span>



| <span data-ttu-id="d0721-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d0721-135">Value</span></span> | <span data-ttu-id="d0721-136">Описание</span><span class="sxs-lookup"><span data-stu-id="d0721-136">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="d0721-137">6</span><span class="sxs-lookup"><span data-stu-id="d0721-137">6</span></span>     | <span data-ttu-id="d0721-138">Подготовка к просмотру с помощью пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d0721-138">Render using the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="d0721-139">7</span><span class="sxs-lookup"><span data-stu-id="d0721-139">7</span></span>     | <span data-ttu-id="d0721-140">Подготовка к просмотру с помощью Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d0721-140">Render using Microsoft DirectShow.</span></span>         |



 

<span data-ttu-id="d0721-141">Изменение значения *времени выполнения* для схемы, ПОДДЕРЖИВАЕМой пакетом SDK формата Windows Media, не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="d0721-141">Changing the *Runtime* value for a scheme that the Windows Media Format SDK supports will have no effect.</span></span> <span data-ttu-id="d0721-142">Проигрыватель всегда будет использовать Windows Media Format SDK в качестве среды выполнения для схем, поддерживаемых пакетом SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d0721-142">The Player will always use the Windows Media Format SDK as the runtime for schemes that the Windows Media Format SDK supports.</span></span> <span data-ttu-id="d0721-143">Это значение реестра позволяет настроить среду выполнения для пользовательских схем.</span><span class="sxs-lookup"><span data-stu-id="d0721-143">This registry value is designed to allow runtime configuration for custom schemes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0721-144">См. также</span><span class="sxs-lookup"><span data-stu-id="d0721-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0721-145">**Параметры реестра**</span><span class="sxs-lookup"><span data-stu-id="d0721-145">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




