---
description: Функция-посредник для метода WebMethod.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: Функция IWICComponentInfo_GetAuthor_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702908"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a><span data-ttu-id="22408-103">\_ \_ Функция прокси Ивиккомпонентинфо-Author</span><span class="sxs-lookup"><span data-stu-id="22408-103">IWICComponentInfo\_GetAuthor\_Proxy function</span></span>

<span data-ttu-id="22408-104">Функция-посредник для [**метода WebMethod**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) .</span><span class="sxs-lookup"><span data-stu-id="22408-104">Proxy function for the [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22408-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22408-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="22408-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22408-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="22408-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22408-108">Тип: \**[**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="22408-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="22408-109">Указатель на этот объект [_ *ивиккомпонентинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="22408-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="22408-110">*кчаусор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22408-110">*cchAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22408-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="22408-111">Type: **UINT**</span></span>

<span data-ttu-id="22408-112">Размер буфера *взаусор* .</span><span class="sxs-lookup"><span data-stu-id="22408-112">The size of the *wzAuthor* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="22408-113">*взаусор* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="22408-113">*wzAuthor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22408-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="22408-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="22408-115">Указатель, получающий имя автора компонента.</span><span class="sxs-lookup"><span data-stu-id="22408-115">A pointer that receives the name of the component's author.</span></span>

<span data-ttu-id="22408-116">Возвращаемая строка зависит от языкового стандарта, 1033 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22408-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="22408-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="22408-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22408-118">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="22408-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="22408-119">Указатель, получающий фактическую длину имени авторов компонента.</span><span class="sxs-lookup"><span data-stu-id="22408-119">A pointer that receives the actual length of the component's authors name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22408-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22408-120">Return value</span></span>

<span data-ttu-id="22408-121">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="22408-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="22408-122">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="22408-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22408-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22408-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22408-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="22408-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="22408-125">Требования</span><span class="sxs-lookup"><span data-stu-id="22408-125">Requirements</span></span>



| <span data-ttu-id="22408-126">Требование</span><span class="sxs-lookup"><span data-stu-id="22408-126">Requirement</span></span> | <span data-ttu-id="22408-127">Значение</span><span class="sxs-lookup"><span data-stu-id="22408-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22408-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22408-128">Minimum supported client</span></span><br/> | <span data-ttu-id="22408-129">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22408-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="22408-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22408-130">Minimum supported server</span></span><br/> | <span data-ttu-id="22408-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22408-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="22408-132">DLL</span><span class="sxs-lookup"><span data-stu-id="22408-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22408-133"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22408-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




