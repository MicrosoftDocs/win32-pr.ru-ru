---
description: Возвращает интерфейсы расширения, которые могут поступать с драйвером устройства для получения образа Windows (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: Метод IWiaItem2::-Extension (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072775"
---
# <a name="iwiaitem2getextension-method"></a><span data-ttu-id="39053-103">Метод IWiaItem2:: Extension</span><span class="sxs-lookup"><span data-stu-id="39053-103">IWiaItem2::GetExtension method</span></span>

<span data-ttu-id="39053-104">Возвращает интерфейсы расширения, которые могут поступать с драйвером устройства для получения образа Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="39053-104">Gets the extension interfaces that might come with a Windows Image Acquisition (WIA) 2.0 device driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="39053-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39053-105">Syntax</span></span>


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a><span data-ttu-id="39053-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39053-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39053-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39053-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39053-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="39053-108">Type: **LONG**</span></span>

<span data-ttu-id="39053-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="39053-109">Currently unused.</span></span> <span data-ttu-id="39053-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="39053-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="39053-111">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39053-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39053-112">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="39053-112">Type: **BSTR**</span></span>

<span data-ttu-id="39053-113">Указывает имя расширения, на которое вызывающее приложение требует указатель на.</span><span class="sxs-lookup"><span data-stu-id="39053-113">Specifies the name of the extension that the calling application requires a pointer to.</span></span>

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span data-ttu-id="39053-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**сегментатионфилтер**</span><span class="sxs-lookup"><span data-stu-id="39053-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span></span>


</dt> <dd>

<span data-ttu-id="39053-115">Расширение фильтра сегментации.</span><span class="sxs-lookup"><span data-stu-id="39053-115">The segmentation filter extension.</span></span> <span data-ttu-id="39053-116">В настоящее время это допустимое значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="39053-116">This is currently the only valid value for this parameter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="39053-117">*риидекстенсионинтерфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39053-117">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39053-118">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="39053-118">Type: **REFIID**</span></span>

<span data-ttu-id="39053-119">Указывает идентификатор интерфейса расширения.</span><span class="sxs-lookup"><span data-stu-id="39053-119">Specifies the identifier of the extension interface.</span></span>

</dd> <dt>

<span data-ttu-id="39053-120">*ппаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39053-120">*ppOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39053-121">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="39053-121">Type: **VOID\*\***</span></span>

<span data-ttu-id="39053-122">Получает адрес указателя на интерфейс расширения.</span><span class="sxs-lookup"><span data-stu-id="39053-122">Receives the address of a pointer to the extension interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39053-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39053-123">Return value</span></span>

<span data-ttu-id="39053-124">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="39053-124">Type: **HRESULT**</span></span>

<span data-ttu-id="39053-125">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="39053-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39053-126">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39053-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39053-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39053-127">Remarks</span></span>

<span data-ttu-id="39053-128">Приложение вызывает этот метод, чтобы создать объект расширения, реализующий один из интерфейсов расширения драйвера WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="39053-128">An application invokes this method to create an extension object implementing one of the WIA 2.0 driver extension interfaces.</span></span> <span data-ttu-id="39053-129">**IWiaItem2:: Extension** сохраняет адрес интерфейса расширения объекта расширения в параметре *риидекстенсионинтерфаце* .</span><span class="sxs-lookup"><span data-stu-id="39053-129">**IWiaItem2::GetExtension** stores the address of the extension object's extension interface in the *riidExtensionInterface* parameter.</span></span> <span data-ttu-id="39053-130">Затем приложение использует указатель интерфейса для вызова его методов.</span><span class="sxs-lookup"><span data-stu-id="39053-130">The application then uses the interface pointer to call its methods.</span></span>

<span data-ttu-id="39053-131">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *риидекстенсионинтерфаце* .</span><span class="sxs-lookup"><span data-stu-id="39053-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *riidExtensionInterface* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="39053-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="39053-132">Examples</span></span>

<span data-ttu-id="39053-133">Креатесегментатионфилтер создает экземпляр фильтра сегментации драйвера ([**ивиасегментатионфилтер**](-wia-iwiasegmentationfilter.md)) путем вызова **IWiaItem2:: Extension** в переданном интерфейсе [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="39053-133">CreateSegmentationFilter creates an instance of the driver's segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) by calling **IWiaItem2::GetExtension** on the passed-in [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span>


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="39053-134">Требования</span><span class="sxs-lookup"><span data-stu-id="39053-134">Requirements</span></span>



| <span data-ttu-id="39053-135">Требование</span><span class="sxs-lookup"><span data-stu-id="39053-135">Requirement</span></span> | <span data-ttu-id="39053-136">Значение</span><span class="sxs-lookup"><span data-stu-id="39053-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39053-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39053-137">Minimum supported client</span></span><br/> | <span data-ttu-id="39053-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39053-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="39053-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39053-139">Minimum supported server</span></span><br/> | <span data-ttu-id="39053-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39053-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="39053-141">Header</span><span class="sxs-lookup"><span data-stu-id="39053-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="39053-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="39053-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="39053-143">IDL</span><span class="sxs-lookup"><span data-stu-id="39053-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39053-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39053-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 
