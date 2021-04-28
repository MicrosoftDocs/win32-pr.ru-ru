---
description: IWICMetadataQueryReader_GetContainerFormat_Proxy функция-прокси для метода Жетконтаинерформат.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: Функция IWICMetadataQueryReader_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097142"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="3ba1b-103">Ивикметадатакуериреадер \_ жетконтаинерформат \_ -функция</span><span class="sxs-lookup"><span data-stu-id="3ba1b-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="3ba1b-104">Функция-посредник для метода [**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="3ba1b-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba1b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ba1b-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3ba1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ba1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba1b-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="3ba1b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba1b-108">Тип: **[ **ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span><span class="sxs-lookup"><span data-stu-id="3ba1b-108">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span></span>

<span data-ttu-id="3ba1b-109">Указатель на этот объект [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="3ba1b-109">Pointer to this [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="3ba1b-110">*пгуидконтаинерформат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ba1b-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ba1b-111">Тип: **GUID \***</span><span class="sxs-lookup"><span data-stu-id="3ba1b-111">Type: **GUID\***</span></span>

<span data-ttu-id="3ba1b-112">Указатель, который получает идентификатор GUID формата коинтаинер.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ba1b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ba1b-113">Return value</span></span>

<span data-ttu-id="3ba1b-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3ba1b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="3ba1b-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3ba1b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ba1b-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ba1b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba1b-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="3ba1b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba1b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3ba1b-118">Requirements</span></span>



| <span data-ttu-id="3ba1b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3ba1b-119">Requirement</span></span> | <span data-ttu-id="3ba1b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3ba1b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba1b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ba1b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba1b-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ba1b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3ba1b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ba1b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba1b-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ba1b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3ba1b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3ba1b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ba1b-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ba1b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




