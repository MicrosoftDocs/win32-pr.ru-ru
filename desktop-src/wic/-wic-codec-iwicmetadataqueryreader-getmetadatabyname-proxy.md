---
description: Функция-посредник для метода Жетметадатабинаме.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: Функция IWICMetadataQueryReader_GetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 96afa63f83e79f399b1c345d38ff2914307c2fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712545"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a><span data-ttu-id="a97f7-103">Ивикметадатакуериреадер \_ жетметадатабинаме \_ -функция</span><span class="sxs-lookup"><span data-stu-id="a97f7-103">IWICMetadataQueryReader\_GetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="a97f7-104">Функция-посредник для метода [**жетметадатабинаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="a97f7-104">Proxy function for the [**GetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a97f7-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="a97f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a97f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97f7-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="a97f7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a97f7-108">Тип: \**[**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="a97f7-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="a97f7-109">Указатель на этот объект [_ *ивикметадатакуериреадер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="a97f7-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="a97f7-110">*взнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a97f7-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a97f7-111">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="a97f7-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="a97f7-112">Имя запрошенного элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="a97f7-112">The name of the requested metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="a97f7-113">*сервер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a97f7-113">*pvarValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a97f7-114">Тип: \**[пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="a97f7-114">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="a97f7-115">Указатель, получающий свойство метаданных.</span><span class="sxs-lookup"><span data-stu-id="a97f7-115">Pointer that receives the metadata property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a97f7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a97f7-116">Return value</span></span>

<span data-ttu-id="a97f7-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a97f7-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a97f7-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a97f7-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a97f7-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a97f7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a97f7-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="a97f7-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a97f7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a97f7-121">Requirements</span></span>



| <span data-ttu-id="a97f7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a97f7-122">Requirement</span></span> | <span data-ttu-id="a97f7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a97f7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a97f7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a97f7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a97f7-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a97f7-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a97f7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a97f7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a97f7-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a97f7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a97f7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a97f7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a97f7-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a97f7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

