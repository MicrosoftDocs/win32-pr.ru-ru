---
description: Проверяет доступность указанного расширения на компьютере и может ли он использоваться методом IWiaItem2::-Extension.
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'Метод IWiaItem2:: Чеккекстенсион (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711249"
---
# <a name="iwiaitem2checkextension-method"></a><span data-ttu-id="a746f-103">Метод IWiaItem2:: Чеккекстенсион</span><span class="sxs-lookup"><span data-stu-id="a746f-103">IWiaItem2::CheckExtension method</span></span>

<span data-ttu-id="a746f-104">Проверяет доступность указанного расширения на компьютере и может ли он использоваться методом [**IWiaItem2::-Extension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="a746f-104">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a746f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a746f-105">Syntax</span></span>


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a><span data-ttu-id="a746f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a746f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a746f-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a746f-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a746f-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="a746f-108">Type: **LONG**</span></span>

<span data-ttu-id="a746f-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="a746f-109">Currently unused.</span></span> <span data-ttu-id="a746f-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a746f-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a746f-111">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a746f-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a746f-112">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a746f-112">Type: **BSTR**</span></span>

<span data-ttu-id="a746f-113">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="a746f-113">Specifies the name of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="a746f-114">*риидекстенсионинтерфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a746f-114">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a746f-115">Тип: **рефиид**</span><span class="sxs-lookup"><span data-stu-id="a746f-115">Type: **REFIID**</span></span>

<span data-ttu-id="a746f-116">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="a746f-116">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="a746f-117">*пбекстенсионексистс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a746f-117">*pbExtensionExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a746f-118">Тип: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="a746f-118">Type: \**BOOL\** _</span></span>

<span data-ttu-id="a746f-119">Получает указатель на _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="a746f-119">Receives a pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="a746f-120"><span id="FALSE"></span><span id="false"></span>**ISFALSE**</span><span class="sxs-lookup"><span data-stu-id="a746f-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="a746f-121">Указанное расширение недоступно.</span><span class="sxs-lookup"><span data-stu-id="a746f-121">The specified extension is not available.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="a746f-122"><span id="TRUE"></span><span id="true"></span>**УСЛОВИЯ**</span><span class="sxs-lookup"><span data-stu-id="a746f-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="a746f-123">Указанное расширение доступно.</span><span class="sxs-lookup"><span data-stu-id="a746f-123">The specified extension is available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a746f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a746f-124">Return value</span></span>

<span data-ttu-id="a746f-125">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a746f-125">Type: **HRESULT**</span></span>

<span data-ttu-id="a746f-126">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a746f-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a746f-127">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a746f-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a746f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a746f-128">Remarks</span></span>

<span data-ttu-id="a746f-129">С помощью этого метода приложения могут проверить, доступно ли расширение, до вызова метода [**IWiaItem2::-Extension**](-wia-iwiaitem2-getextension.md) .</span><span class="sxs-lookup"><span data-stu-id="a746f-129">Using this method, applications can check whether an extension is available before calling the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <span data-ttu-id="a746f-130">Кроме того, приложение может проверить, какие расширения доступны без совместного создания, а затем решить, какой из них следует использовать.</span><span class="sxs-lookup"><span data-stu-id="a746f-130">Also, the application can check which extensions are available without co-creating each of them, and then decide which one to use.</span></span>

## <a name="examples"></a><span data-ttu-id="a746f-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="a746f-131">Examples</span></span>

<span data-ttu-id="a746f-132">Чеккимгфилтер проверяет, имеет ли драйвер фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="a746f-132">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="a746f-133">Перед вызовом компонента предварительной версии приложение должно убедиться, что драйвер имеет фильтр обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="a746f-133">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a><span data-ttu-id="a746f-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a746f-134">Requirements</span></span>



| <span data-ttu-id="a746f-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a746f-135">Requirement</span></span> | <span data-ttu-id="a746f-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a746f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a746f-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a746f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a746f-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a746f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a746f-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a746f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a746f-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a746f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a746f-141">Header</span><span class="sxs-lookup"><span data-stu-id="a746f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a746f-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a746f-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a746f-143">IDL</span><span class="sxs-lookup"><span data-stu-id="a746f-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a746f-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a746f-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 




