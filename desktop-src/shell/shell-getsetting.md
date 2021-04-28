---
description: Метод Shell.-Setting — получает параметр глобальной оболочки.
ms.assetid: 3E8C7C6A-5696-4756-B4BF-902FA2420AE9
title: Метод Shell.-Setting (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: dc8fe6277208808ad5f5b182f3eee416daf4a5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083742"
---
# <a name="shellgetsetting-method"></a><span data-ttu-id="ebd21-103">Shell. метод Setting</span><span class="sxs-lookup"><span data-stu-id="ebd21-103">Shell.GetSetting method</span></span>

<span data-ttu-id="ebd21-104">Извлекает параметр глобальной оболочки.</span><span class="sxs-lookup"><span data-stu-id="ebd21-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd21-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebd21-105">Syntax</span></span>


```JScript
retVal = Shell.GetSetting(
  lSetting
)
```


```VB

Shell.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="ebd21-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebd21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd21-107">*лсеттинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ebd21-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd21-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="ebd21-108">Type: **long**</span></span>

<span data-ttu-id="ebd21-109">Значение типа, указывающее текущий параметр оболочки для извлечения.</span><span class="sxs-lookup"><span data-stu-id="ebd21-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="ebd21-110">В каждом вызове можно получить только один параметр.</span><span class="sxs-lookup"><span data-stu-id="ebd21-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="ebd21-111">Этот метод распознает следующие значения.</span><span class="sxs-lookup"><span data-stu-id="ebd21-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="ebd21-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**ССФ \_ АУТОЧЕККСЕЛЕКТ** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-113">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="ebd21-113">**Windows Vista and later**.</span></span> <span data-ttu-id="ebd21-114">Состояние флажков " **использовать" для выбора элементов** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="ebd21-115">Этот параметр включается автоматически, если в системе настроено устройство ввода с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="ebd21-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="ebd21-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**ССФ \_ ДЕСКТОФТМЛ** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="ebd21-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ebd21-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="ebd21-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**ССФ \_ ДОНТПРЕТТИПАС** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="ebd21-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-119">Состояние параметра **Разрешить все прописные имена** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="ebd21-120">В Windows Vista этот параметр папки больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="ebd21-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="ebd21-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**ССФ \_ ДАУБЛЕКЛИККИНВЕБВИЕВ** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="ebd21-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-122">Состояние **двойного щелчка для открытия элемента (одиночный щелчок для выбора)** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="ebd21-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**ССФ \_ ФИЛЬТР** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ebd21-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="ebd21-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**ССФ \_ ХИДДЕНФИЛИКСТС** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="ebd21-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ebd21-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="ebd21-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**ССФ \_ ХИДЕИКОНС** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-128">Состояние значка отображается в представлении списка проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="ebd21-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="ebd21-129">Если этот параметр активен, значки в представлении списка не отображаются.</span><span class="sxs-lookup"><span data-stu-id="ebd21-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="ebd21-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**ССФ \_ ИКОНСОНЛИ** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-131">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="ebd21-131">**Windows Vista and later**.</span></span> <span data-ttu-id="ebd21-132">Состояние отображаемого имени отображается в представлении списка проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="ebd21-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="ebd21-133">Если этот параметр активен, значки отображаются в представлении списка, а отображаемые имена — нет.</span><span class="sxs-lookup"><span data-stu-id="ebd21-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="ebd21-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**ССФ \_ МАПНЕТДРВБУТТОН** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-135">Состояние **кнопки показывать сетевой диск в параметре панели инструментов** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="ebd21-136">Начиная с Windows Vista этот параметр больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="ebd21-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="ebd21-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**ССФ \_ НОКОНФИРМРЕЦИКЛЕ** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-138">Состояние параметра **диалогового окна подтверждения удаления** из корзины.</span><span class="sxs-lookup"><span data-stu-id="ebd21-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="ebd21-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**ССФ \_ НОНЕТКРАВЛИНГ** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-140">Состояние параметра **автоматически искать сетевые папки и принтеры** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="ebd21-141">Начиная с Windows Vista этот параметр больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="ebd21-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="ebd21-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**ССФ \_ СЕППРОЦЕСС** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-143">Состояние **окна запуска папки в отдельном** параметре обработки.</span><span class="sxs-lookup"><span data-stu-id="ebd21-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="ebd21-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**ССФ \_ СЕРВЕРАДМИНУИ** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="ebd21-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-145">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ebd21-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="ebd21-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**ССФ \_ ШОВАЛЛОБЖЕКТС** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ebd21-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-147">Состояние параметра **скрытые файлы и папки** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="ebd21-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**ССФ \_ ШОВАТТРИБКОЛ** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="ebd21-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-149">Состояние параметра **Показать атрибуты файла в подробном представлении** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="ebd21-150">Начиная с Windows Vista этот параметр больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="ebd21-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="ebd21-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**ССФ \_ ШОВКОМПКОЛОР** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="ebd21-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-152">Состояние параметра **Показывать зашифрованные или сжатые файлы NTFS в цвете** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="ebd21-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**ССФ \_ ШОВЕКСТЕНСИОНС** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ebd21-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-154">Состояние параметра **Скрывать расширения для известных типов файлов** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="ebd21-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**ССФ \_ ШОВИНФОТИП** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-156">Состояние параметра **Показать всплывающее описание для папок и элементов рабочего стола** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="ebd21-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**ССФ \_ ШОВСТАРТПАЖЕ** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-158">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ebd21-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="ebd21-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**ССФ \_ ШОВСУПЕРХИДДЕН** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-160">Состояние параметра **Скрывать защищенные системные файлы** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="ebd21-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**ССФ \_ ШОВСИСФИЛЕС** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="ebd21-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-162">Состояние параметра **скрытые файлы и папки** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="ebd21-163">В Windows Vista и более поздних версиях это эквивалентно ССФ \_ шоваллобжектс.</span><span class="sxs-lookup"><span data-stu-id="ebd21-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="ebd21-164">В версиях Windows, предшествующих Windows Vista, это значение ссылается на состояние параметра не **Показывать скрытые файлы и папки** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="ebd21-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**ССФ \_ ШОВТИПЕОВЕРЛАЙ** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-166">**Windows Vista и более поздние версии**.</span><span class="sxs-lookup"><span data-stu-id="ebd21-166">**Windows Vista and later**.</span></span> <span data-ttu-id="ebd21-167">Состояние **значка отображаемого файла в параметре эскизов** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="ebd21-168">Если этот параметр активен, то при указании файла в виде эскиза применяется наложение типа файла.</span><span class="sxs-lookup"><span data-stu-id="ebd21-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="ebd21-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**ССФ \_ СОРТКОЛУМНС** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="ebd21-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-170">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ebd21-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="ebd21-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**ССФ \_ СТАРТПАНЕЛОН** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-172">Состояние параметра отображения Windows XP, которое выбирает между стилем Windows XP и классическим стилем.</span><span class="sxs-lookup"><span data-stu-id="ebd21-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="ebd21-173">Начиная с Windows Vista этот параметр больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="ebd21-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="ebd21-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**ССФ \_ WEBVIEW** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="ebd21-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-175">Состояние **отображения в виде веб-представления**.</span><span class="sxs-lookup"><span data-stu-id="ebd21-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="ebd21-176">Начиная с Windows Vista этот параметр больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="ebd21-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="ebd21-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**ССФ \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="ebd21-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="ebd21-178">Состояние параметра **классического стиля** .</span><span class="sxs-lookup"><span data-stu-id="ebd21-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="ebd21-179">Начиная с Windows Vista этот параметр больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="ebd21-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd21-180">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebd21-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ebd21-181">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="ebd21-181">JScript</span></span>

<span data-ttu-id="ebd21-182">Тип: **Variant \_ bool \***</span><span class="sxs-lookup"><span data-stu-id="ebd21-182">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="ebd21-183">Задайте значение **true** , если параметр существует. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ebd21-183">Set to **true** if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ebd21-184">VB</span><span class="sxs-lookup"><span data-stu-id="ebd21-184">VB</span></span>

<span data-ttu-id="ebd21-185">Тип: **Variant \_ bool \***</span><span class="sxs-lookup"><span data-stu-id="ebd21-185">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="ebd21-186">Задайте значение **true** , если параметр существует. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ebd21-186">Set to **true** if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="ebd21-187">Примеры</span><span class="sxs-lookup"><span data-stu-id="ebd21-187">Examples</span></span>

<span data-ttu-id="ebd21-188">В следующих примерах показано использование **параметра Setting** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ebd21-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ebd21-189">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="ebd21-189">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="ebd21-190">Сценариев</span><span class="sxs-lookup"><span data-stu-id="ebd21-190">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
```



<span data-ttu-id="ebd21-191">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ebd21-191">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ebd21-192">Требования</span><span class="sxs-lookup"><span data-stu-id="ebd21-192">Requirements</span></span>



| <span data-ttu-id="ebd21-193">Требование</span><span class="sxs-lookup"><span data-stu-id="ebd21-193">Requirement</span></span> | <span data-ttu-id="ebd21-194">Значение</span><span class="sxs-lookup"><span data-stu-id="ebd21-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd21-195">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebd21-195">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd21-196">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ebd21-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ebd21-197">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebd21-197">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd21-198">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ebd21-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ebd21-199">Header</span><span class="sxs-lookup"><span data-stu-id="ebd21-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebd21-200"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebd21-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ebd21-201">IDL</span><span class="sxs-lookup"><span data-stu-id="ebd21-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ebd21-202"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ebd21-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ebd21-203">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd21-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd21-204"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ebd21-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




