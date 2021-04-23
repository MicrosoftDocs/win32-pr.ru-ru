---
description: Таблица Мсишорткутпроперти позволяет установщику окон задавать свойства для ярлыков, которые также являются объектами оболочки Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Таблица Мсишорткутпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546423"
---
# <a name="msishortcutproperty-table"></a><span data-ttu-id="e75fc-103">Таблица Мсишорткутпроперти</span><span class="sxs-lookup"><span data-stu-id="e75fc-103">MsiShortcutProperty Table</span></span>

<span data-ttu-id="e75fc-104">Таблица Мсишорткутпроперти позволяет установщику окон задавать свойства для ярлыков, которые также являются объектами [оболочки Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e75fc-104">The MsiShortcutProperty table enables Window Installer to set properties for shortcuts that are also [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) objects.</span></span> <span data-ttu-id="e75fc-105">Начиная с Windows Vista и Windows Server 2008 оболочка Windows предоставляет интерфейс Ипропертисторе для объектов оболочки, таких как ярлыки.</span><span class="sxs-lookup"><span data-stu-id="e75fc-105">Beginning with Windows Vista and Windows Server 2008 the Windows Shell provides an IPropertyStore Interface for shell objects such as shortcuts.</span></span> <span data-ttu-id="e75fc-106">Пакет установщик Windows 5,0, выполняющийся в Windows Server 2008 R2 или Windows 7, может устанавливать эти свойства при установке ярлыка.</span><span class="sxs-lookup"><span data-stu-id="e75fc-106">A Windows Installer 5.0 package running on Windows Server 2008 R2 or Windows 7 can set these properties when the shortcut is installed.</span></span>

<span data-ttu-id="e75fc-107">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e75fc-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="e75fc-108">Эта таблица доступна начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="e75fc-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="e75fc-109">Таблица Мсишорткутпроперти содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="e75fc-109">The MsiShortcutProperty table has the following columns.</span></span>



| <span data-ttu-id="e75fc-110">Столбец</span><span class="sxs-lookup"><span data-stu-id="e75fc-110">Column</span></span>              | <span data-ttu-id="e75fc-111">Type</span><span class="sxs-lookup"><span data-stu-id="e75fc-111">Type</span></span>                         | <span data-ttu-id="e75fc-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="e75fc-112">Key</span></span> | <span data-ttu-id="e75fc-113">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="e75fc-113">Nullable</span></span> |
|---------------------|------------------------------|-----|----------|
| <span data-ttu-id="e75fc-114">мсишорткутпроперти</span><span class="sxs-lookup"><span data-stu-id="e75fc-114">MsiShortcutProperty</span></span> | [<span data-ttu-id="e75fc-115">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e75fc-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="e75fc-116">Да</span><span class="sxs-lookup"><span data-stu-id="e75fc-116">Y</span></span>   | <span data-ttu-id="e75fc-117">Нет</span><span class="sxs-lookup"><span data-stu-id="e75fc-117">N</span></span>        |
| <span data-ttu-id="e75fc-118">Сочетание клавиш\_</span><span class="sxs-lookup"><span data-stu-id="e75fc-118">Shortcut\_</span></span>          | [<span data-ttu-id="e75fc-119">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e75fc-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="e75fc-120">Нет</span><span class="sxs-lookup"><span data-stu-id="e75fc-120">N</span></span>   | <span data-ttu-id="e75fc-121">Нет</span><span class="sxs-lookup"><span data-stu-id="e75fc-121">N</span></span>        |
| <span data-ttu-id="e75fc-122">PropertyKey</span><span class="sxs-lookup"><span data-stu-id="e75fc-122">PropertyKey</span></span>         | [<span data-ttu-id="e75fc-123">Формате</span><span class="sxs-lookup"><span data-stu-id="e75fc-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e75fc-124">Нет</span><span class="sxs-lookup"><span data-stu-id="e75fc-124">N</span></span>   | <span data-ttu-id="e75fc-125">Нет</span><span class="sxs-lookup"><span data-stu-id="e75fc-125">N</span></span>        |
| <span data-ttu-id="e75fc-126">пропвариантвалуе</span><span class="sxs-lookup"><span data-stu-id="e75fc-126">PropVariantValue</span></span>    | [<span data-ttu-id="e75fc-127">Формате</span><span class="sxs-lookup"><span data-stu-id="e75fc-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e75fc-128">Нет</span><span class="sxs-lookup"><span data-stu-id="e75fc-128">N</span></span>   | <span data-ttu-id="e75fc-129">Нет</span><span class="sxs-lookup"><span data-stu-id="e75fc-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e75fc-130">Столбцы</span><span class="sxs-lookup"><span data-stu-id="e75fc-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e75fc-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>мсишорткутпроперти</span><span class="sxs-lookup"><span data-stu-id="e75fc-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span></span>
</dt> <dd>

<span data-ttu-id="e75fc-132">Уникальный идентификатор для этой строки таблицы Мсишорткутпроперти.</span><span class="sxs-lookup"><span data-stu-id="e75fc-132">Unique identifier for this row of the MsiShortcutProperty table.</span></span>

</dd> <dt>

<span data-ttu-id="e75fc-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Сочетания\_</span><span class="sxs-lookup"><span data-stu-id="e75fc-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Shortcut\_</span></span>
</dt> <dd>

<span data-ttu-id="e75fc-134">Ключ в таблице [ярлыков](shortcut-table.md) , который определяет ярлык с набором свойств.</span><span class="sxs-lookup"><span data-stu-id="e75fc-134">A key into the [Shortcut](shortcut-table.md) table that identifies the shortcut having a property set.</span></span>

</dd> <dt>

<span data-ttu-id="e75fc-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span><span class="sxs-lookup"><span data-stu-id="e75fc-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span></span>
</dt> <dd>

<span data-ttu-id="e75fc-136">Строковое значение, предоставляющее сведения для структуры [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) .</span><span class="sxs-lookup"><span data-stu-id="e75fc-136">A string value that provides information for the [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="e75fc-137">Сведения в этом поле должны ссылаться на каноническое имя свойства, зарегистрированное в системе свойств Windows.</span><span class="sxs-lookup"><span data-stu-id="e75fc-137">The information in this field must refer to the canonical name of a property registered with the Windows property system.</span></span> <span data-ttu-id="e75fc-138">Дополнительные сведения о системе свойств Windows см. в разделе Общие сведения о [системе свойств](/previous-versions//bb776909(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e75fc-138">For more information about the Windows property system, see the [Property System Overview](/previous-versions//bb776909(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e75fc-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>пропвариантвалуе</span><span class="sxs-lookup"><span data-stu-id="e75fc-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span></span>
</dt> <dd>

<span data-ttu-id="e75fc-140">Строковое значение, предоставляющее сведения для структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="e75fc-140">A string value that provides information for the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

</dd> </dl>

<span data-ttu-id="e75fc-141">Для ярлыка можно задать несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="e75fc-141">Multiple properties can be set on a shortcut.</span></span> <span data-ttu-id="e75fc-142">Если одно и то же свойство задано несколько раз для одного и того же сочетания клавиш, оно устанавливается в неопределенном порядке.</span><span class="sxs-lookup"><span data-stu-id="e75fc-142">If the same property is set multiple times on the same shortcut the value is set in an unspecified order.</span></span>

<span data-ttu-id="e75fc-143">Установщик Windows могут устанавливать свойства ярлыка только при установке или переустановке ярлыка.</span><span class="sxs-lookup"><span data-stu-id="e75fc-143">Windows Installer can set shortcut properties only when the shortcut is installed or reinstalled.</span></span> <span data-ttu-id="e75fc-144">Исправление, которое не устанавливает уже установленный ярлык, не обновляет свойства ярлыка.</span><span class="sxs-lookup"><span data-stu-id="e75fc-144">A patch that does not reinstall a shortcut that has already been installed does not update the shortcut's properties.</span></span> <span data-ttu-id="e75fc-145">Исправление может обновить свойства, включив в пакет исправлений таблицу [ярлыков](shortcut-table.md) и переустановив ярлык.</span><span class="sxs-lookup"><span data-stu-id="e75fc-145">A patch can update the properties by including a [Shortcut](shortcut-table.md) table in the patch package and reinstalling the shortcut.</span></span>

## <a name="remarks"></a><span data-ttu-id="e75fc-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e75fc-146">Remarks</span></span>

<span data-ttu-id="e75fc-147">[Установщик Windows сообщение об ошибке](windows-installer-error-messages.md) 1946 возвращается в виде предупреждения, и установка будет продолжена, если установщик Windows не удается задать свойство ярлыка, указанное в таблице мсишорткутпроперти.</span><span class="sxs-lookup"><span data-stu-id="e75fc-147">[Windows Installer Error Message](windows-installer-error-messages.md) 1946 is returned as a warning, and the installation continues, if Windows Installer is unable to set a shortcut property specified in the MsiShortcutProperty table.</span></span>

## <a name="validation"></a><span data-ttu-id="e75fc-148">Проверка</span><span class="sxs-lookup"><span data-stu-id="e75fc-148">Validation</span></span>

<dl>

[<span data-ttu-id="e75fc-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="e75fc-149">ICE03</span></span>](ice03.md)  
</dl>

 

 
