---
description: Функция-посредник для метода класса CLSID.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: Функция IWICComponentInfo_GetCLSID_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc63d3f30605c0f5343502bcb96e989cc8496540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703325"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a><span data-ttu-id="6e568-103">\_ \_ Функция прокси ИВИККОМПОНЕНТИНФО-CLSID</span><span class="sxs-lookup"><span data-stu-id="6e568-103">IWICComponentInfo\_GetCLSID\_Proxy function</span></span>

<span data-ttu-id="6e568-104">Функция-посредник для метода [**класса CLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) .</span><span class="sxs-lookup"><span data-stu-id="6e568-104">Proxy function for the [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e568-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e568-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a><span data-ttu-id="6e568-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e568-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e568-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="6e568-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e568-108">Тип: \**[**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="6e568-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="6e568-109">Указатель на этот объект [_ *ивиккомпонентинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="6e568-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="6e568-110">*пклсид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6e568-110">*pclsid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e568-111">Тип: \**CLSID \** _</span><span class="sxs-lookup"><span data-stu-id="6e568-111">Type: \**CLSID\** _</span></span>

<span data-ttu-id="6e568-112">Указатель, получающий CLSID компонента.</span><span class="sxs-lookup"><span data-stu-id="6e568-112">A pointer that receives the component's CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e568-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e568-113">Return value</span></span>

<span data-ttu-id="6e568-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6e568-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6e568-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e568-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e568-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e568-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e568-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="6e568-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6e568-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6e568-118">Requirements</span></span>



| <span data-ttu-id="6e568-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6e568-119">Requirement</span></span> | <span data-ttu-id="6e568-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6e568-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e568-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e568-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e568-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e568-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6e568-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e568-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e568-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e568-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6e568-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e568-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e568-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e568-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




