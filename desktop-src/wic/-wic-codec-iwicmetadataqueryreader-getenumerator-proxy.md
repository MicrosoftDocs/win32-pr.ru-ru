---
description: Функция-посредник для метода GetEnumerator.
ms.assetid: b45b240d-7540-4115-ac8b-401aaf400a9d
title: Функция IWICMetadataQueryReader_GetEnumerator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetEnumerator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a549cfb31691a32d1a7be76e1b051740ecf64e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674227"
---
# <a name="iwicmetadataqueryreader_getenumerator_proxy-function"></a><span data-ttu-id="61997-103">\_ \_ Функция-посредник ивикметадатакуериреадер GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="61997-103">IWICMetadataQueryReader\_GetEnumerator\_Proxy function</span></span>

<span data-ttu-id="61997-104">Функция-посредник для метода [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) .</span><span class="sxs-lookup"><span data-stu-id="61997-104">Proxy function for the [**GetEnumerator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61997-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61997-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetEnumerator_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ IEnumString             **ppIEnumString
);
```



## <a name="parameters"></a><span data-ttu-id="61997-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61997-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61997-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="61997-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61997-108">Тип: \**[**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="61997-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="61997-109">Указатель на этот объект [_ *ивикметадатакуериреадер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="61997-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="61997-110">*ппиенумстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61997-110">*ppIEnumString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61997-111">Тип: **иенумстринг \* \***</span><span class="sxs-lookup"><span data-stu-id="61997-111">Type: **IEnumString\*\***</span></span>

<span data-ttu-id="61997-112">Указатель, получающий указатель на перечислитель метаданных.</span><span class="sxs-lookup"><span data-stu-id="61997-112">A pointer that receives a pointer to a metadata enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61997-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61997-113">Return value</span></span>

<span data-ttu-id="61997-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="61997-114">Type: **HRESULT**</span></span>

<span data-ttu-id="61997-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="61997-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61997-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61997-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61997-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="61997-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="61997-118">Требования</span><span class="sxs-lookup"><span data-stu-id="61997-118">Requirements</span></span>



| <span data-ttu-id="61997-119">Требование</span><span class="sxs-lookup"><span data-stu-id="61997-119">Requirement</span></span> | <span data-ttu-id="61997-120">Значение</span><span class="sxs-lookup"><span data-stu-id="61997-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61997-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61997-121">Minimum supported client</span></span><br/> | <span data-ttu-id="61997-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61997-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="61997-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61997-123">Minimum supported server</span></span><br/> | <span data-ttu-id="61997-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61997-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="61997-125">DLL</span><span class="sxs-lookup"><span data-stu-id="61997-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61997-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61997-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




