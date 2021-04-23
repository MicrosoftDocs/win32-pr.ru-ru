---
description: Функция-посредник для метода Lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: Функция IWICBitmap_Lock_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673269"
---
# <a name="iwicbitmap_lock_proxy-function"></a><span data-ttu-id="9d9e4-103">Ивикбитмап \_ Lock \_ -функция</span><span class="sxs-lookup"><span data-stu-id="9d9e4-103">IWICBitmap\_Lock\_Proxy function</span></span>

<span data-ttu-id="9d9e4-104">Функция-посредник для метода [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) .</span><span class="sxs-lookup"><span data-stu-id="9d9e4-104">Proxy function for the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d9e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d9e4-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a><span data-ttu-id="9d9e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d9e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d9e4-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="9d9e4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9e4-108">Тип: \**[**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="9d9e4-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="9d9e4-109">Указатель на этот объект [_ *ивикбитмап* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="9d9e4-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="9d9e4-110">*прклокк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d9e4-110">*prcLock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9e4-111">Тип: \**const [**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="9d9e4-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="9d9e4-112">Прямоугольник, к которому осуществляется доступ.</span><span class="sxs-lookup"><span data-stu-id="9d9e4-112">The rectangle to be accessed.</span></span>

</dd> <dt>

<span data-ttu-id="9d9e4-113">_flags \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9d9e4-113">_flags\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9e4-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9d9e4-114">Type: **DWORD**</span></span>

<span data-ttu-id="9d9e4-115">Режим доступа, который вы хотите получить для блокировки.</span><span class="sxs-lookup"><span data-stu-id="9d9e4-115">The access mode you wish to obtain for the lock.</span></span>

</dd> <dt>

<span data-ttu-id="9d9e4-116">*ппилокк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9d9e4-116">*ppILock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9e4-117">Тип: **[ **ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span><span class="sxs-lookup"><span data-stu-id="9d9e4-117">Type: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span></span>

<span data-ttu-id="9d9e4-118">Указатель, получающий заблокированную область памяти.</span><span class="sxs-lookup"><span data-stu-id="9d9e4-118">A pointer that receives the locked memory location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d9e4-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d9e4-119">Return value</span></span>

<span data-ttu-id="9d9e4-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9d9e4-120">Type: **HRESULT**</span></span>

<span data-ttu-id="9d9e4-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9d9e4-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d9e4-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d9e4-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d9e4-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="9d9e4-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9e4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9d9e4-124">Requirements</span></span>



| <span data-ttu-id="9d9e4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9d9e4-125">Requirement</span></span> | <span data-ttu-id="9d9e4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9d9e4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9e4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d9e4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9e4-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d9e4-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9d9e4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d9e4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9e4-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d9e4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9d9e4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9d9e4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d9e4-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d9e4-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




