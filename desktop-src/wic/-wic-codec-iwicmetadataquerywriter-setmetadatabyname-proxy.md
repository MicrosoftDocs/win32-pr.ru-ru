---
description: Функция-посредник для метода Сетметадатабинаме.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: Функция IWICMetadataQueryWriter_SetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712569"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a><span data-ttu-id="19ecd-103">Ивикметадатакуеривритер \_ сетметадатабинаме \_ -функция</span><span class="sxs-lookup"><span data-stu-id="19ecd-103">IWICMetadataQueryWriter\_SetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="19ecd-104">Функция-посредник для метода [**сетметадатабинаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="19ecd-104">Proxy function for the [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ecd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19ecd-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="19ecd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19ecd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ecd-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="19ecd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ecd-108">Тип: \**[**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="19ecd-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="19ecd-109">Указатель на этот объект [_ *ивикметадатакуеривритер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="19ecd-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="19ecd-110">*взнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19ecd-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ecd-111">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="19ecd-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="19ecd-112">Имя элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="19ecd-112">The name of the metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="19ecd-113">*сервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19ecd-113">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ecd-114">Тип: \**const [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="19ecd-114">Type: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="19ecd-115">Заданные метаданные.</span><span class="sxs-lookup"><span data-stu-id="19ecd-115">The metadata to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ecd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19ecd-116">Return value</span></span>

<span data-ttu-id="19ecd-117">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="19ecd-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="19ecd-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="19ecd-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19ecd-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19ecd-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19ecd-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="19ecd-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="19ecd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="19ecd-121">Requirements</span></span>



| <span data-ttu-id="19ecd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="19ecd-122">Requirement</span></span> | <span data-ttu-id="19ecd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="19ecd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19ecd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19ecd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19ecd-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19ecd-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="19ecd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19ecd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19ecd-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19ecd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="19ecd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="19ecd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19ecd-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19ecd-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

