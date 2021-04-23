---
description: Функция-посредник для метода Жетметадатакуериреадер.
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: Функция IWICBitmapDecoder_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343222"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="c62e6-103">Ивикбитмапдекодер \_ жетметадатакуериреадер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="c62e6-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="c62e6-104">Функция-посредник для метода [**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="c62e6-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c62e6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="c62e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c62e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c62e6-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="c62e6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c62e6-108">Тип: \**[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="c62e6-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="c62e6-109">Указатель на этот объект [_ *ивикбитмапдекодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="c62e6-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="c62e6-110">*ппиметадатакуериреадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c62e6-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c62e6-111">Тип: **[ **ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="c62e6-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="c62e6-112">Указатель, получающий указатель на метаданные.</span><span class="sxs-lookup"><span data-stu-id="c62e6-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c62e6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c62e6-113">Return value</span></span>

<span data-ttu-id="c62e6-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c62e6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c62e6-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c62e6-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c62e6-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c62e6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c62e6-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="c62e6-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c62e6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c62e6-118">Requirements</span></span>



| <span data-ttu-id="c62e6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c62e6-119">Requirement</span></span> | <span data-ttu-id="c62e6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c62e6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62e6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c62e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c62e6-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c62e6-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c62e6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c62e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c62e6-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c62e6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c62e6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c62e6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c62e6-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c62e6-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




