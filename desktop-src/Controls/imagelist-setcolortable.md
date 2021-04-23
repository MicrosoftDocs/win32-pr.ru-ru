---
title: Функция ImageList_SetColorTable
description: Задает таблицу цветов для списка изображений.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- Функции ImageList_SetColorTable элементов управления Windows
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989455"
---
# <a name="imagelist_setcolortable-function"></a><span data-ttu-id="c2e2c-104">Сетколортабле ImageList, \_ функция</span><span class="sxs-lookup"><span data-stu-id="c2e2c-104">ImageList\_SetColorTable function</span></span>

<span data-ttu-id="c2e2c-105">Задает таблицу цветов для списка изображений.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-105">Sets the color table for an image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e2c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2e2c-106">Syntax</span></span>


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a><span data-ttu-id="c2e2c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2e2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e2c-108">*химл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2e2c-108">*himl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e2c-109">Тип: **химажелист**</span><span class="sxs-lookup"><span data-stu-id="c2e2c-109">Type: **HIMAGELIST**</span></span>

<span data-ttu-id="c2e2c-110">Маркер списка изображений.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-110">A handle to the image list.</span></span>

</dd> <dt>

<span data-ttu-id="c2e2c-111">*Запуск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2e2c-111">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e2c-112">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="c2e2c-112">Type: **int**</span></span>

<span data-ttu-id="c2e2c-113">Индекс таблицы цветов, начинающийся с нуля, указывающий первую заданную запись в таблице цветов.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-113">A zero-based color table index that specifies the first color table entry to set.</span></span>

</dd> <dt>

<span data-ttu-id="c2e2c-114">*Len* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2e2c-114">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e2c-115">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="c2e2c-115">Type: **int**</span></span>

<span data-ttu-id="c2e2c-116">Число заданных записей в таблице цветов.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-116">The number of color table entries to set.</span></span>

</dd> <dt>

<span data-ttu-id="c2e2c-117">*пргб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2e2c-117">*prgb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e2c-118">Тип: \**[**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _</span><span class="sxs-lookup"><span data-stu-id="c2e2c-118">Type: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\** _</span></span>

<span data-ttu-id="c2e2c-119">Указатель на массив структур _len \* [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , содержащий новые сведения о цвете для таблицы цветов DIB.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-119">A pointer to an array of _len\* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures containing new color information for the color table of the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e2c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2e2c-120">Return value</span></span>

<span data-ttu-id="c2e2c-121">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="c2e2c-121">Type: **int**</span></span>

<span data-ttu-id="c2e2c-122">Если функция выполнена, возвращается число записей в таблице цветов, заданных функцией.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-122">If the function succeeds, it returns the number of color table entries set by the function.</span></span> <span data-ttu-id="c2e2c-123">Если функция завершается ошибкой, возвращаемое значение меньше или равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-123">If the function fails, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e2c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2e2c-124">Remarks</span></span>

<span data-ttu-id="c2e2c-125">Только списки изображений, созданные с помощью флага [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) или [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) , имеют таблицы цветов.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-125">Only image lists created with the [**ILC\_COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) or [**ILC\_COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) flag have color tables.</span></span> <span data-ttu-id="c2e2c-126">Цветовая таблица такого списка изображений обычно устанавливается автоматически путем копирования таблицы цветов первого изображения, добавленного в список (например, с помощью функции [**\_ Add ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ), если это изображение имеет формат DIB.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-126">The color table of such an image list is typically set automatically by copying the color table of the first image added to the list (for example, through the [**ImageList\_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) function) if that image is a DIB.</span></span> <span data-ttu-id="c2e2c-127">Если первое изображение, добавленное в список изображений, не является DIB, то таблица цветов палитры полутонового изображения используется для **ILC \_ COLOR8** , а таблица цветов VGA используется для **ILC \_ COLOR4**.</span><span class="sxs-lookup"><span data-stu-id="c2e2c-127">If the first image added to the image list is not a DIB, then the color table of the halftone palette is used for **ILC\_COLOR8** image lists and the VGA color table is used for **ILC\_COLOR4**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e2c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c2e2c-128">Requirements</span></span>



| <span data-ttu-id="c2e2c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c2e2c-129">Requirement</span></span> | <span data-ttu-id="c2e2c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c2e2c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e2c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2e2c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e2c-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2e2c-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="c2e2c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2e2c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e2c-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2e2c-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c2e2c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c2e2c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2e2c-136"><dt>Comctl32.dll (версия 3,51 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e2c-136"><dt>Comctl32.dll (version 3.51 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e2c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2e2c-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2e2c-138">[Таблица цветов](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="c2e2c-138">[Color Table](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span></span>
</dt> </dl>

 

