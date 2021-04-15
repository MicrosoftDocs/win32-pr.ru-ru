---
description: Определяет данные, необходимые для вызова диалогового окна устройства.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Структура ДЕВИЦЕДИАЛОГДАТА (Виадефд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545567"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="a5b3f-103">Структура ДЕВИЦЕДИАЛОГДАТА</span><span class="sxs-lookup"><span data-stu-id="a5b3f-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="a5b3f-104">Определяет данные, необходимые для вызова диалогового окна устройства.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b3f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5b3f-105">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a><span data-ttu-id="a5b3f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a5b3f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5b3f-107">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a5b3f-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a5b3f-109">Задает размер этой структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a5b3f-110">**хвндпарент**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="a5b3f-111">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="a5b3f-112">Задает маркер родительского окна диалога.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="a5b3f-113">**пивиаитемрут**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="a5b3f-114">Тип: \**[**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _</span><span class="sxs-lookup"><span data-stu-id="a5b3f-114">Type: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\** _</span></span>

</dd> <dd>

<span data-ttu-id="a5b3f-115">Указывает на интерфейс [_ *ивиаитем* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) , представляющий допустимый корневой элемент в дереве элементов приложения.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-115">Points to an [_ *IWiaItem*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="a5b3f-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a5b3f-117">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a5b3f-118">Задает набор флагов, управляющих работой диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="a5b3f-119">Можно задать любое из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a5b3f-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="a5b3f-120">Flag</span><span class="sxs-lookup"><span data-stu-id="a5b3f-120">Flag</span></span>                                 | <span data-ttu-id="a5b3f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a5b3f-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b3f-122">0</span><span class="sxs-lookup"><span data-stu-id="a5b3f-122">0</span></span>                                    | <span data-ttu-id="a5b3f-123">Поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="a5b3f-124">\_ \_ \_ одиночное изображение диалогового окна WIA устройства \_</span><span class="sxs-lookup"><span data-stu-id="a5b3f-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="a5b3f-125">Ограничить выбор изображения одним изображением в диалоговом окне "получение образа устройства".</span><span class="sxs-lookup"><span data-stu-id="a5b3f-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="a5b3f-126">\_ \_ \_ \_ Общий \_ Пользовательский интерфейс диалогового окна устройства WIA</span><span class="sxs-lookup"><span data-stu-id="a5b3f-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="a5b3f-127">Используйте пользовательский интерфейс системы, если он доступен, а не пользовательский интерфейс, предоставляемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="a5b3f-128">Если пользовательский интерфейс системы недоступен, используется пользовательский интерфейс поставщика.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="a5b3f-129">Если ни один из ИНТЕРФЕЙСов не доступен, функция возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a5b3f-130">**линтент**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="a5b3f-131">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="a5b3f-132">Указывает, какой тип данных должен представлять изображение.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="a5b3f-133">Список значений намерения образа см. в разделе [**константы намерения изображения**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="a5b3f-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5b3f-134">**литемкаунт**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="a5b3f-135">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="a5b3f-136">Получает число элементов в массиве, указанное параметром **ппвиаитем** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a5b3f-137">**ппвиаитем**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="a5b3f-138">Тип: **[ **ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="a5b3f-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="a5b3f-139">Получает адрес массива указателей на интерфейсы [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5b3f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="a5b3f-140">Requirements</span></span>



| <span data-ttu-id="a5b3f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="a5b3f-141">Requirement</span></span> | <span data-ttu-id="a5b3f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="a5b3f-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b3f-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5b3f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b3f-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a5b3f-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5b3f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b3f-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a5b3f-147">Header</span><span class="sxs-lookup"><span data-stu-id="a5b3f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b3f-148"><dt>Виадефд. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b3f-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




