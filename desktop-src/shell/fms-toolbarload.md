---
description: Содержит сведения о настраиваемых кнопках, добавляемых на панель инструментов диспетчера файлов. Кнопки предоставляются БИБЛИОТЕКой расширения диспетчера файлов.
title: Структура FMS_TOOLBARLOAD (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842165"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="3baec-104">\_Структура FMS тулбарлоад</span><span class="sxs-lookup"><span data-stu-id="3baec-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="3baec-105">Содержит сведения о настраиваемых кнопках, добавляемых на панель инструментов диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="3baec-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="3baec-106">Кнопки предоставляются БИБЛИОТЕКой расширения диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="3baec-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="3baec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3baec-107">Syntax</span></span>


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a><span data-ttu-id="3baec-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3baec-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3baec-109">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="3baec-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="3baec-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3baec-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3baec-111">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="3baec-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="3baec-112">Диспетчер файлов задает размер перед вызовом расширения и проверяет размер после возврата процедуры расширения.</span><span class="sxs-lookup"><span data-stu-id="3baec-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="3baec-113">**лпбуттонс**</span><span class="sxs-lookup"><span data-stu-id="3baec-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="3baec-114">Тип: **\_ кнопка лпекст**</span><span class="sxs-lookup"><span data-stu-id="3baec-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="3baec-115">Адрес массива структур [**\_ кнопок ext**](ext-button.md) .</span><span class="sxs-lookup"><span data-stu-id="3baec-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="3baec-116">**кбуттонс**</span><span class="sxs-lookup"><span data-stu-id="3baec-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="3baec-117">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="3baec-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3baec-118">Количество структур [**\_ кнопок ext**](ext-button.md) в массиве, на которое указывает элемент **лпбуттонс** .</span><span class="sxs-lookup"><span data-stu-id="3baec-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="3baec-119">Это число равно количеству кнопок и разделителей, добавляемых на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="3baec-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="3baec-120">**кбитмапс**</span><span class="sxs-lookup"><span data-stu-id="3baec-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="3baec-121">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="3baec-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3baec-122">Количество кнопок, представленных заданным растровым изображением.</span><span class="sxs-lookup"><span data-stu-id="3baec-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="3baec-123">**идбитмап**</span><span class="sxs-lookup"><span data-stu-id="3baec-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="3baec-124">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="3baec-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3baec-125">Идентификатор ресурса точечного рисунка в исполняемом файле для библиотеки DLL расширения.</span><span class="sxs-lookup"><span data-stu-id="3baec-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="3baec-126">Ресурс точечного рисунка содержит изображения для количества кнопок, заданных параметром **кбитмапс**.</span><span class="sxs-lookup"><span data-stu-id="3baec-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="3baec-127">Диспетчер файлов загружает ресурс точечного рисунка, а затем использует его для вывода кнопок.</span><span class="sxs-lookup"><span data-stu-id="3baec-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="3baec-128">**хбитмап**</span><span class="sxs-lookup"><span data-stu-id="3baec-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="3baec-129">Тип: **хбитмап**</span><span class="sxs-lookup"><span data-stu-id="3baec-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="3baec-130">Маркер точечного рисунка, который диспетчер файлов будет использовать для получения и просмотра изображений кнопок, если **идбитмап** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="3baec-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3baec-131">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="3baec-131">Requirements</span></span>



| <span data-ttu-id="3baec-132">Требование</span><span class="sxs-lookup"><span data-stu-id="3baec-132">Requirement</span></span> | <span data-ttu-id="3baec-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3baec-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3baec-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3baec-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3baec-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3baec-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3baec-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3baec-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3baec-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3baec-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3baec-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3baec-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3baec-139"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="3baec-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3baec-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3baec-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3baec-141">**ФМЕВЕНТ \_ тулбарлоад**</span><span class="sxs-lookup"><span data-stu-id="3baec-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




