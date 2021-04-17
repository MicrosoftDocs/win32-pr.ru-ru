---
title: Метод Исофткбд Креатесофткэйбоардлайаутфромресаурце (Софткбдк. h)
description: Метод Исофткбд Креатесофткэйббоардлайаутфромресаурце создает раскладку с мягкими клавиатурами из указанного ресурса.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Платформа служб текстового ввода метода Креатесофткэйбоардлайаутфромресаурце
- Платформа текстовых служб метода Креатесофткэйбоардлайаутфромресаурце, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Креатесофткэйбоардлайаутфромресаурце
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682003"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a><span data-ttu-id="14994-106">Метод Исофткбд:: Креатесофткэйбоардлайаутфромресаурце</span><span class="sxs-lookup"><span data-stu-id="14994-106">ISoftKbd::CreateSoftKeyboardLayoutFromResource method</span></span>

<span data-ttu-id="14994-107">Метод **исофткбд:: креатесофткэйббоардлайаутфромресаурце** создает раскладку с экранной клавиатурой из указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="14994-107">The **ISoftKbd::CreateSoftKeybboardLayoutFromResource** method creates a soft keyboard layout from the specified resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="14994-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14994-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="14994-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="14994-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14994-110">*лпсзресфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14994-110">*lpszResFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14994-111">Указатель на строку, завершающуюся нулем, указывающую имя файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14994-111">Pointer to a zero-terminated string indicating the name of the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="14994-112">*лпсзрестипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14994-112">*lpszResType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14994-113">Указатель на строку, завершающуюся нулем, указывающую тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="14994-113">Pointer to a zero-terminated string indicating the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="14994-114">*лпсзксмлресстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14994-114">*lpszXMLResString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14994-115">Указатель на строку, завершающуюся нулем, обозначающую ресурс.</span><span class="sxs-lookup"><span data-stu-id="14994-115">Pointer to a zero-terminated string identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="14994-116">*лпдвлайауткукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="14994-116">*lpdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14994-117">Указатель на буфер, в котором этот метод получает куки-файл раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="14994-117">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14994-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14994-118">Return value</span></span>

<span data-ttu-id="14994-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="14994-119">This method can return one of these values.</span></span>



| <span data-ttu-id="14994-120">Значение</span><span class="sxs-lookup"><span data-stu-id="14994-120">Value</span></span>                                                                                        | <span data-ttu-id="14994-121">Описание</span><span class="sxs-lookup"><span data-stu-id="14994-121">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="14994-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="14994-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="14994-123">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="14994-123">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="14994-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="14994-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="14994-125">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="14994-125">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="14994-126">Требования</span><span class="sxs-lookup"><span data-stu-id="14994-126">Requirements</span></span>



| <span data-ttu-id="14994-127">Требование</span><span class="sxs-lookup"><span data-stu-id="14994-127">Requirement</span></span> | <span data-ttu-id="14994-128">Значение</span><span class="sxs-lookup"><span data-stu-id="14994-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14994-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14994-129">Minimum supported client</span></span><br/> | <span data-ttu-id="14994-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14994-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="14994-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14994-131">Minimum supported server</span></span><br/> | <span data-ttu-id="14994-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14994-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14994-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="14994-133">Redistributable</span></span><br/>          | <span data-ttu-id="14994-134">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="14994-134">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="14994-135">Header</span><span class="sxs-lookup"><span data-stu-id="14994-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="14994-136"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="14994-136"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="14994-137">IDL</span><span class="sxs-lookup"><span data-stu-id="14994-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14994-138"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14994-138"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="14994-139">DLL</span><span class="sxs-lookup"><span data-stu-id="14994-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14994-140"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14994-140"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14994-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14994-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14994-142">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="14994-142">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="14994-143">**Исофткбд:: Креатесофткэйбоардлайаутфромксмлфиле**</span><span class="sxs-lookup"><span data-stu-id="14994-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[<span data-ttu-id="14994-144">**Исофткбд:: Шовсофткэйбоард**</span><span class="sxs-lookup"><span data-stu-id="14994-144">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





