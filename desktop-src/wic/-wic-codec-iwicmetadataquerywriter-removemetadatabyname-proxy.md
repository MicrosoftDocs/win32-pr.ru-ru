---
description: Функция-посредник для метода Ремовеметадатабинаме.
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: Функция IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911148"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a><span data-ttu-id="be3be-103">Ивикметадатакуеривритер \_ ремовеметадатабинаме \_ -функция</span><span class="sxs-lookup"><span data-stu-id="be3be-103">IWICMetadataQueryWriter\_RemoveMetadataByName\_Proxy function</span></span>

<span data-ttu-id="be3be-104">Функция-посредник для метода [**ремовеметадатабинаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="be3be-104">Proxy function for the [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be3be-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a><span data-ttu-id="be3be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be3be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be3be-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="be3be-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3be-108">Тип: \**[**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="be3be-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="be3be-109">Указатель на этот объект [_ *ивикметадатакуеривритер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="be3be-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="be3be-110">*взнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be3be-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3be-111">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="be3be-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="be3be-112">Имя удаляемого элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="be3be-112">The name of the metadata item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be3be-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be3be-113">Return value</span></span>

<span data-ttu-id="be3be-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="be3be-114">Type: **HRESULT**</span></span>

<span data-ttu-id="be3be-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="be3be-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be3be-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be3be-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3be-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="be3be-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="be3be-118">Требования</span><span class="sxs-lookup"><span data-stu-id="be3be-118">Requirements</span></span>



| <span data-ttu-id="be3be-119">Требование</span><span class="sxs-lookup"><span data-stu-id="be3be-119">Requirement</span></span> | <span data-ttu-id="be3be-120">Значение</span><span class="sxs-lookup"><span data-stu-id="be3be-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be3be-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be3be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be3be-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be3be-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="be3be-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be3be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be3be-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be3be-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="be3be-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be3be-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be3be-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be3be-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




