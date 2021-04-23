---
title: Метод Исофткбд Креатесофткэйбоардлайаутфромксмлфиле (Софткбдк. h)
description: Метод Исофткбд Креатесофткэйбоардлайаутфромксмлфиле создает раскладку экранной клавиатуры из указанного XML-файла.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Платформа служб текстового ввода метода Креатесофткэйбоардлайаутфромксмлфиле
- Платформа текстовых служб метода Креатесофткэйбоардлайаутфромксмлфиле, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Креатесофткэйбоардлайаутфромксмлфиле
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682002"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a><span data-ttu-id="39539-106">Метод Исофткбд:: Креатесофткэйбоардлайаутфромксмлфиле</span><span class="sxs-lookup"><span data-stu-id="39539-106">ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile method</span></span>

<span data-ttu-id="39539-107">Метод **исофткбд:: креатесофткэйбоардлайаутфромксмлфиле** создает раскладку экранной клавиатуры из указанного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="39539-107">The **ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** method creates a soft keyboard layout from the specified XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="39539-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39539-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="39539-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="39539-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39539-110">*лпсзкэйбоарддесфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39539-110">*lpszKeyboardDesFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39539-111">Указатель на строку, завершающуюся нулем, указывающую имя XML-файла.</span><span class="sxs-lookup"><span data-stu-id="39539-111">Pointer to a zero-terminated string indicating the name of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="39539-112">*сзфилестрлен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39539-112">*szFileStrLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39539-113">Строка, завершающаяся нулем, указывающая длину XML-файла.</span><span class="sxs-lookup"><span data-stu-id="39539-113">Zero-terminated string indicating the length of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="39539-114">*пдвлайауткукие* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39539-114">*pdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39539-115">Указатель на буфер, в котором этот метод получает куки-файл раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="39539-115">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39539-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39539-116">Return value</span></span>

<span data-ttu-id="39539-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="39539-117">This method can return one of these values.</span></span>



| <span data-ttu-id="39539-118">Значение</span><span class="sxs-lookup"><span data-stu-id="39539-118">Value</span></span>                                                                                        | <span data-ttu-id="39539-119">Описание</span><span class="sxs-lookup"><span data-stu-id="39539-119">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="39539-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="39539-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="39539-121">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="39539-121">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="39539-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="39539-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="39539-123">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="39539-123">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39539-124">Требования</span><span class="sxs-lookup"><span data-stu-id="39539-124">Requirements</span></span>



| <span data-ttu-id="39539-125">Требование</span><span class="sxs-lookup"><span data-stu-id="39539-125">Requirement</span></span> | <span data-ttu-id="39539-126">Значение</span><span class="sxs-lookup"><span data-stu-id="39539-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39539-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39539-127">Minimum supported client</span></span><br/> | <span data-ttu-id="39539-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39539-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39539-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39539-129">Minimum supported server</span></span><br/> | <span data-ttu-id="39539-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39539-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="39539-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="39539-131">Redistributable</span></span><br/>          | <span data-ttu-id="39539-132">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="39539-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="39539-133">Header</span><span class="sxs-lookup"><span data-stu-id="39539-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="39539-134"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="39539-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="39539-135">IDL</span><span class="sxs-lookup"><span data-stu-id="39539-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39539-136"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39539-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="39539-137">DLL</span><span class="sxs-lookup"><span data-stu-id="39539-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39539-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39539-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39539-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39539-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39539-140">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="39539-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="39539-141">**Исофткбд:: Креатесофткэйбоардлайаутфромресаурце**</span><span class="sxs-lookup"><span data-stu-id="39539-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





