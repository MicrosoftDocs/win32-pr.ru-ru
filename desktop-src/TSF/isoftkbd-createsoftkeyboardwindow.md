---
title: Метод Исофткбд Креатесофткэйбоардвиндов (Софткбдк. h)
description: Метод Исофткбд Креатесофткэйбоардвиндов создает окно с экранной клавиатурой.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Платформа служб текстового ввода метода Креатесофткэйбоардвиндов
- Платформа текстовых служб метода Креатесофткэйбоардвиндов, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Креатесофткэйбоардвиндов
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534793"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a><span data-ttu-id="b597b-106">Метод Исофткбд:: Креатесофткэйбоардвиндов</span><span class="sxs-lookup"><span data-stu-id="b597b-106">ISoftKbd::CreateSoftKeyboardWindow method</span></span>

<span data-ttu-id="b597b-107">Метод **исофткбд:: креатесофткэйбоардвиндов** создает окно с экранной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="b597b-107">The **ISoftKbd::CreateSoftKeyboardWindow** method creates a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b597b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b597b-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a><span data-ttu-id="b597b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b597b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b597b-110">*ховнер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b597b-110">*hOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b597b-111">Маркер окна, в котором будет содержаться мягкая клавиатура.</span><span class="sxs-lookup"><span data-stu-id="b597b-111">Handle of the window to contain the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="b597b-112">*\_ Тип заголовка* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="b597b-112">*Titlebar\_type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b597b-113">Тип заголовка окна экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b597b-113">Type of title bar for the soft keyboard window.</span></span> <span data-ttu-id="b597b-114">Возможные типы определяются перечислением [**\_ типа в строке заголовка**](titlebar-type.md) .</span><span class="sxs-lookup"><span data-stu-id="b597b-114">Possible types are defined by the [**TITLEBAR\_TYPE**](titlebar-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="b597b-115">*кспос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b597b-115">*xPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b597b-116">Координата по оси x верхнего левого угла окна экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b597b-116">The x position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="b597b-117">*ИПОС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b597b-117">*yPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b597b-118">Координата y левого верхнего угла окна экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b597b-118">The y position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="b597b-119">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b597b-119">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b597b-120">Ширина окна экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b597b-120">The width of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="b597b-121">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b597b-121">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b597b-122">Высота окна экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="b597b-122">The height of the soft keyboard window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b597b-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b597b-123">Return value</span></span>

<span data-ttu-id="b597b-124">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b597b-124">This method can return one of these values.</span></span>



| <span data-ttu-id="b597b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b597b-125">Value</span></span>                                                                                        | <span data-ttu-id="b597b-126">Описание</span><span class="sxs-lookup"><span data-stu-id="b597b-126">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b597b-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b597b-127"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b597b-128">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="b597b-128">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="b597b-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b597b-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b597b-130">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="b597b-130">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b597b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b597b-131">Requirements</span></span>



| <span data-ttu-id="b597b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b597b-132">Requirement</span></span> | <span data-ttu-id="b597b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b597b-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b597b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b597b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b597b-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b597b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b597b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b597b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b597b-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b597b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b597b-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b597b-138">Redistributable</span></span><br/>          | <span data-ttu-id="b597b-139">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="b597b-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="b597b-140">Header</span><span class="sxs-lookup"><span data-stu-id="b597b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b597b-141"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b597b-141"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="b597b-142">IDL</span><span class="sxs-lookup"><span data-stu-id="b597b-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b597b-143"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b597b-143"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="b597b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b597b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b597b-145"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b597b-145"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b597b-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b597b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b597b-147">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="b597b-147">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="b597b-148">**Исофткбд:: Креатесофткэйбоардлайаутфромресаурце**</span><span class="sxs-lookup"><span data-stu-id="b597b-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[<span data-ttu-id="b597b-149">**Исофткбд::D Естройсофткэйбоардвиндов**</span><span class="sxs-lookup"><span data-stu-id="b597b-149">**ISoftKbd::DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[<span data-ttu-id="b597b-150">**Исофткбд:: Шовсофткэйбоард**</span><span class="sxs-lookup"><span data-stu-id="b597b-150">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[<span data-ttu-id="b597b-151">**Тип заголовка окна \_**</span><span class="sxs-lookup"><span data-stu-id="b597b-151">**TITLEBAR\_TYPE**</span></span>](titlebar-type.md)
</dt> </dl>

 

 





