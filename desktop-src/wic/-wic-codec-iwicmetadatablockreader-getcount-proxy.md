---
description: Функция-посредник для метода NOCOUNT.
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: Функция IWICMetadataBlockReader_GetCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265998"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a><span data-ttu-id="85ff3-103">\_ \_ Функция прокси-сервера ивикметадатаблоккреадер NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="85ff3-103">IWICMetadataBlockReader\_GetCount\_Proxy function</span></span>

<span data-ttu-id="85ff3-104">Функция-посредник для метода [**NOCOUNT**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) .</span><span class="sxs-lookup"><span data-stu-id="85ff3-104">Proxy function for the [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ff3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85ff3-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="85ff3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85ff3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ff3-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="85ff3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ff3-108">Тип: \**[**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="85ff3-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="85ff3-109">Указатель на этот объект [_ *ивикметадатаблоккреадер* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="85ff3-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="85ff3-110">*пккаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="85ff3-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ff3-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="85ff3-111">Type: \**UINT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ff3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85ff3-112">Return value</span></span>

<span data-ttu-id="85ff3-113">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="85ff3-113">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="85ff3-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="85ff3-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85ff3-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85ff3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85ff3-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="85ff3-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="85ff3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="85ff3-117">Requirements</span></span>



| <span data-ttu-id="85ff3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="85ff3-118">Requirement</span></span> | <span data-ttu-id="85ff3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="85ff3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ff3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85ff3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85ff3-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85ff3-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="85ff3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85ff3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85ff3-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85ff3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="85ff3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="85ff3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85ff3-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85ff3-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




