---
description: Класс Win32 \_ десктопвми представляет общие характеристики рабочего стола пользователя. Свойства этого класса могут быть изменены пользователем для настройки рабочего стола.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Класс Win32_Desktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896486"
---
# <a name="win32_desktop-class"></a><span data-ttu-id="4231f-104">\_Класс рабочего стола Win32</span><span class="sxs-lookup"><span data-stu-id="4231f-104">Win32\_Desktop class</span></span>

<span data-ttu-id="4231f-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) для **\_ настольных компьютеров Win32** представляет общие характеристики рабочего стола пользователя.</span><span class="sxs-lookup"><span data-stu-id="4231f-105">The **Win32\_Desktop**[WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the common characteristics of a user's desktop.</span></span> <span data-ttu-id="4231f-106">Свойства этого класса могут быть изменены пользователем для настройки рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="4231f-106">The properties of this class can be modified by the user to customize the desktop.</span></span>

<span data-ttu-id="4231f-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4231f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4231f-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4231f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4231f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4231f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a><span data-ttu-id="4231f-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4231f-110">Members</span></span>

<span data-ttu-id="4231f-111">Класс **\_ рабочего стола Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4231f-111">The **Win32\_Desktop** class has these types of members:</span></span>

-   [<span data-ttu-id="4231f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4231f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4231f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4231f-113">Properties</span></span>

<span data-ttu-id="4231f-114">Класс **\_ рабочего стола Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4231f-114">The **Win32\_Desktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4231f-115">**BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="4231f-115">**BorderWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-116">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4231f-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| BorderWidth ")</span><span class="sxs-lookup"><span data-stu-id="4231f-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|BorderWidth")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-119">Ширина границ вокруг всех окон с изменяемыми границами.</span><span class="sxs-lookup"><span data-stu-id="4231f-119">Width of the borders around all windows with adjustable borders.</span></span>

<span data-ttu-id="4231f-120">Пример: 3</span><span class="sxs-lookup"><span data-stu-id="4231f-120">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="4231f-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="4231f-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-124">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4231f-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4231f-125">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="4231f-125">Short textual description of the current object.</span></span>

<span data-ttu-id="4231f-126">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="4231f-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4231f-127">**кулсвитч**</span><span class="sxs-lookup"><span data-stu-id="4231f-127">**CoolSwitch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4231f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-130">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| кулсвитч")</span><span class="sxs-lookup"><span data-stu-id="4231f-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CoolSwitch")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-131">Включено быстрое переключение задач.</span><span class="sxs-lookup"><span data-stu-id="4231f-131">Fast task switching is turned on.</span></span> <span data-ttu-id="4231f-132">Быстрое переключение задач позволяет пользователю переключаться между окнами с помощью сочетания клавиш **ALT + TAB** .</span><span class="sxs-lookup"><span data-stu-id="4231f-132">Fast task switching allows the user to switch between windows using the **ALT+TAB** keyboard combination.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-133">**курсорблинкрате**</span><span class="sxs-lookup"><span data-stu-id="4231f-133">**CursorBlinkRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4231f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| курсорблинкрате"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="4231f-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CursorBlinkRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-137">Промежуток времени между мигающими последовательными курсорами.</span><span class="sxs-lookup"><span data-stu-id="4231f-137">Length of time between successive cursor blinks.</span></span>

<span data-ttu-id="4231f-138">Пример: 530</span><span class="sxs-lookup"><span data-stu-id="4231f-138">Example: 530</span></span>

</dd> <dt>

<span data-ttu-id="4231f-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4231f-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4231f-142">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="4231f-142">Textual description of the current object.</span></span>

<span data-ttu-id="4231f-143">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="4231f-143">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4231f-144">**драгфуллвиндовс**</span><span class="sxs-lookup"><span data-stu-id="4231f-144">**DragFullWindows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4231f-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-147">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| драгфуллвиндовс")</span><span class="sxs-lookup"><span data-stu-id="4231f-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|DragFullWindows")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-148">Содержимое окна отображается, когда пользователь перемещает окно.</span><span class="sxs-lookup"><span data-stu-id="4231f-148">Contents of a window are shown when a user moves the window.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-149">**гридгрануларити**</span><span class="sxs-lookup"><span data-stu-id="4231f-149">**GridGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4231f-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-152">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Панель управления \\ \\ Desktop \| гридгрануларити"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 пикселей")</span><span class="sxs-lookup"><span data-stu-id="4231f-152">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|GridGranularity"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-153">Пространство сетки, к которой привязаны окна на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="4231f-153">Spacing of the grid that windows are bound to on the desktop.</span></span> <span data-ttu-id="4231f-154">Это упрощает организацию окон.</span><span class="sxs-lookup"><span data-stu-id="4231f-154">This makes organizing windows easier.</span></span> <span data-ttu-id="4231f-155">Как правило, отступы достаточно точно, чтобы пользователь не заметит его.</span><span class="sxs-lookup"><span data-stu-id="4231f-155">The spacing is usually fine enough that the user does not notice it.</span></span>

<span data-ttu-id="4231f-156">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="4231f-156">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="4231f-157">**иконспаЦинг**</span><span class="sxs-lookup"><span data-stu-id="4231f-157">**IconSpacing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-158">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4231f-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-160">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| иконспаЦинг "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="4231f-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-161">Интервал между значками.</span><span class="sxs-lookup"><span data-stu-id="4231f-161">Spacing between icons.</span></span>

<span data-ttu-id="4231f-162">Пример: 75</span><span class="sxs-lookup"><span data-stu-id="4231f-162">Example: 75</span></span>

</dd> <dt>

<span data-ttu-id="4231f-163">**иконтитлефаценаме**</span><span class="sxs-lookup"><span data-stu-id="4231f-163">**IconTitleFaceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-166">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| иконфонт ")</span><span class="sxs-lookup"><span data-stu-id="4231f-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconFont")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-167">Шрифт, используемый для имен значков.</span><span class="sxs-lookup"><span data-stu-id="4231f-167">Font used for the names of the icons.</span></span>

<span data-ttu-id="4231f-168">Пример: "MS San Serif"</span><span class="sxs-lookup"><span data-stu-id="4231f-168">Example: "MS San Serif"</span></span>

</dd> <dt>

<span data-ttu-id="4231f-169">**иконтитлесизе**</span><span class="sxs-lookup"><span data-stu-id="4231f-169">**IconTitleSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4231f-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-172">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Font and Text Structures \| [**Логфонтв**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| лфхеигхт"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Point")</span><span class="sxs-lookup"><span data-stu-id="4231f-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Font and Text Structures\|[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)\|lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-173">Размер шрифта значка.</span><span class="sxs-lookup"><span data-stu-id="4231f-173">Icon font size.</span></span>

<span data-ttu-id="4231f-174">Пример: 9</span><span class="sxs-lookup"><span data-stu-id="4231f-174">Example: 9</span></span>

</dd> <dt>

<span data-ttu-id="4231f-175">**иконтитлеврап**</span><span class="sxs-lookup"><span data-stu-id="4231f-175">**IconTitleWrap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-176">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4231f-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-178">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \\ \\ виндовметрикс \| иконтитлеврап ")</span><span class="sxs-lookup"><span data-stu-id="4231f-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconTitleWrap")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-179">Текст заголовка значка переносится на следующую строку.</span><span class="sxs-lookup"><span data-stu-id="4231f-179">Icon's title text wraps to the next line.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-180">**Name**</span><span class="sxs-lookup"><span data-stu-id="4231f-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-183">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="4231f-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-184">Имя, идентифицирующее текущий профиль рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="4231f-184">Name that identifies the current desktop profile.</span></span>

<span data-ttu-id="4231f-185">Пример: "Маинпроф"</span><span class="sxs-lookup"><span data-stu-id="4231f-185">Example: "MainProf"</span></span>

</dd> <dt>

<span data-ttu-id="4231f-186">**Шаблон**</span><span class="sxs-lookup"><span data-stu-id="4231f-186">**Pattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-189">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Шаблон рабочего стола панели управления по умолчанию \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="4231f-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Pattern")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-190">Имя шаблона, используемого в качестве фона для рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="4231f-190">Name of the pattern used as the background for the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-191">**скринсаверактиве**</span><span class="sxs-lookup"><span data-stu-id="4231f-191">**ScreenSaverActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-192">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4231f-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-194">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| скринсавеактиве ")</span><span class="sxs-lookup"><span data-stu-id="4231f-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveActive")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-195">Экранная заставка активна.</span><span class="sxs-lookup"><span data-stu-id="4231f-195">Screen saver is active.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-196">**скринсаверексекутабле**</span><span class="sxs-lookup"><span data-stu-id="4231f-196">**ScreenSaverExecutable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-199">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Панель управления \\ \\SCRNSAVE.EXE рабочего стола по умолчанию \| ")</span><span class="sxs-lookup"><span data-stu-id="4231f-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|SCRNSAVE.EXE")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-200">Имя текущего исполняемого файла экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="4231f-200">Name of the current screen saver executable file.</span></span>

<span data-ttu-id="4231f-201">Пример: "LOGON. SCR</span><span class="sxs-lookup"><span data-stu-id="4231f-201">Example: "LOGON.SCR"</span></span>

</dd> <dt>

<span data-ttu-id="4231f-202">**скринсаверсекуре**</span><span class="sxs-lookup"><span data-stu-id="4231f-202">**ScreenSaverSecure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-203">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4231f-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-205">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| скринсавериссекуре ")</span><span class="sxs-lookup"><span data-stu-id="4231f-205">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaverIsSecure")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-206">Пароль включен для экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="4231f-206">Password is enabled for the screen saver.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-207">**скринсавертимеаут**</span><span class="sxs-lookup"><span data-stu-id="4231f-207">**ScreenSaverTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4231f-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-210">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| скринсаветимеаут "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" секунды ")</span><span class="sxs-lookup"><span data-stu-id="4231f-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-211">Период времени, прошедший до запуска заставки экрана.</span><span class="sxs-lookup"><span data-stu-id="4231f-211">Amount of time that passes before the screen saver starts.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-212">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="4231f-212">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-215">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4231f-215">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4231f-216">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="4231f-216">Identifier by which the current object is known.</span></span>

<span data-ttu-id="4231f-217">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="4231f-217">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4231f-218">**Фоновый рисунок**</span><span class="sxs-lookup"><span data-stu-id="4231f-218">**Wallpaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4231f-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-221">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Рисунок рабочего стола панели управления по умолчанию \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="4231f-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Wallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-222">Имя файла для фона рабочего стола в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="4231f-222">File name for the wallpaper design on the background of the desktop.</span></span>

<span data-ttu-id="4231f-223">Пример: "WINNT.BMP"</span><span class="sxs-lookup"><span data-stu-id="4231f-223">Example: "WINNT.BMP"</span></span>

</dd> <dt>

<span data-ttu-id="4231f-224">**валлпаперстретчед**</span><span class="sxs-lookup"><span data-stu-id="4231f-224">**WallpaperStretched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-225">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4231f-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-227">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| валлпаперстиле ")</span><span class="sxs-lookup"><span data-stu-id="4231f-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|WallpaperStyle")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-228">Фоновый рисунок растягивается для заполнения всего экрана.</span><span class="sxs-lookup"><span data-stu-id="4231f-228">Wallpaper is stretched to fill the entire screen.</span></span> <span data-ttu-id="4231f-229">Microsoft Plus!</span><span class="sxs-lookup"><span data-stu-id="4231f-229">Microsoft Plus!</span></span> <span data-ttu-id="4231f-230">необходимо установить, прежде чем этот параметр станет доступен.</span><span class="sxs-lookup"><span data-stu-id="4231f-230">must be installed before this option is available.</span></span> <span data-ttu-id="4231f-231">Если задано **значение false**, фоновый рисунок оставляет свои исходные размеры на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="4231f-231">If **FALSE**, the wallpaper retains its original dimensions on the desktop background.</span></span>

</dd> <dt>

<span data-ttu-id="4231f-232">**валлпапертилед**</span><span class="sxs-lookup"><span data-stu-id="4231f-232">**WallpaperTiled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4231f-233">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4231f-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4231f-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4231f-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4231f-235">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Панель управления по УМОЛЧАНИю \\ \\ \\ \\ Desktop \| тилеваллпапер ")</span><span class="sxs-lookup"><span data-stu-id="4231f-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|TileWallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="4231f-236">Фоновый рисунок накладывается или выравнивается по центру.</span><span class="sxs-lookup"><span data-stu-id="4231f-236">Wallpaper is tiled or centered.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4231f-237">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4231f-237">Remarks</span></span>

<span data-ttu-id="4231f-238">Класс **\_ рабочего стола Win32** является производным [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="4231f-238">The **Win32\_Desktop** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="4231f-239">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="4231f-239">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="4231f-240">Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="4231f-240">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="4231f-241">Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="4231f-241">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="4231f-242">Примеры</span><span class="sxs-lookup"><span data-stu-id="4231f-242">Examples</span></span>

<span data-ttu-id="4231f-243">В следующем примере кода показано, как получить сведения о рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="4231f-243">The following code sample describes how to retrieve desktop information.</span></span>


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a><span data-ttu-id="4231f-244">Требования</span><span class="sxs-lookup"><span data-stu-id="4231f-244">Requirements</span></span>



| <span data-ttu-id="4231f-245">Требование</span><span class="sxs-lookup"><span data-stu-id="4231f-245">Requirement</span></span> | <span data-ttu-id="4231f-246">Значение</span><span class="sxs-lookup"><span data-stu-id="4231f-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4231f-247">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4231f-247">Minimum supported client</span></span><br/> | <span data-ttu-id="4231f-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4231f-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4231f-249">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4231f-249">Minimum supported server</span></span><br/> | <span data-ttu-id="4231f-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4231f-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4231f-251">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4231f-251">Namespace</span></span><br/>                | <span data-ttu-id="4231f-252">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4231f-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4231f-253">MOF</span><span class="sxs-lookup"><span data-stu-id="4231f-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4231f-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4231f-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4231f-255">DLL</span><span class="sxs-lookup"><span data-stu-id="4231f-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4231f-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4231f-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4231f-257">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4231f-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4231f-258">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="4231f-258">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="4231f-259">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4231f-259">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

