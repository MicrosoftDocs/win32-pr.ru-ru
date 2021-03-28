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
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985508"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="f16d3-104">\_Структура FMS тулбарлоад</span><span class="sxs-lookup"><span data-stu-id="f16d3-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="f16d3-105">Содержит сведения о настраиваемых кнопках, добавляемых на панель инструментов диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="f16d3-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="f16d3-106">Кнопки предоставляются БИБЛИОТЕКой расширения диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="f16d3-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16d3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f16d3-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="f16d3-108">Участники</span><span class="sxs-lookup"><span data-stu-id="f16d3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f16d3-109">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="f16d3-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="f16d3-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f16d3-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f16d3-111">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="f16d3-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="f16d3-112">Диспетчер файлов задает размер перед вызовом расширения и проверяет размер после возврата процедуры расширения.</span><span class="sxs-lookup"><span data-stu-id="f16d3-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="f16d3-113">**лпбуттонс**</span><span class="sxs-lookup"><span data-stu-id="f16d3-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="f16d3-114">Тип: **\_ кнопка лпекст**</span><span class="sxs-lookup"><span data-stu-id="f16d3-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="f16d3-115">Адрес массива структур [**\_ кнопок ext**](ext-button.md) .</span><span class="sxs-lookup"><span data-stu-id="f16d3-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="f16d3-116">**кбуттонс**</span><span class="sxs-lookup"><span data-stu-id="f16d3-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="f16d3-117">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="f16d3-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f16d3-118">Количество структур [**\_ кнопок ext**](ext-button.md) в массиве, на которое указывает элемент **лпбуттонс** .</span><span class="sxs-lookup"><span data-stu-id="f16d3-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="f16d3-119">Это число равно количеству кнопок и разделителей, добавляемых на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="f16d3-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="f16d3-120">**кбитмапс**</span><span class="sxs-lookup"><span data-stu-id="f16d3-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="f16d3-121">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="f16d3-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f16d3-122">Количество кнопок, представленных заданным растровым изображением.</span><span class="sxs-lookup"><span data-stu-id="f16d3-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f16d3-123">**идбитмап**</span><span class="sxs-lookup"><span data-stu-id="f16d3-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="f16d3-124">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="f16d3-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f16d3-125">Идентификатор ресурса точечного рисунка в исполняемом файле для библиотеки DLL расширения.</span><span class="sxs-lookup"><span data-stu-id="f16d3-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="f16d3-126">Ресурс точечного рисунка содержит изображения для количества кнопок, заданных параметром **кбитмапс**.</span><span class="sxs-lookup"><span data-stu-id="f16d3-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="f16d3-127">Диспетчер файлов загружает ресурс точечного рисунка, а затем использует его для вывода кнопок.</span><span class="sxs-lookup"><span data-stu-id="f16d3-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="f16d3-128">**хбитмап**</span><span class="sxs-lookup"><span data-stu-id="f16d3-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="f16d3-129">Тип: **хбитмап**</span><span class="sxs-lookup"><span data-stu-id="f16d3-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="f16d3-130">Маркер точечного рисунка, который диспетчер файлов будет использовать для получения и просмотра изображений кнопок, если **идбитмап** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="f16d3-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f16d3-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f16d3-131">Requirements</span></span>



| <span data-ttu-id="f16d3-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f16d3-132">Requirement</span></span> | <span data-ttu-id="f16d3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f16d3-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f16d3-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f16d3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f16d3-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f16d3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f16d3-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f16d3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f16d3-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f16d3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f16d3-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f16d3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f16d3-139"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16d3-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16d3-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f16d3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16d3-141">**ФМЕВЕНТ \_ тулбарлоад**</span><span class="sxs-lookup"><span data-stu-id="f16d3-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




