---
description: Функция-посредник для метода Жетдатапоинтер.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: Функция IWICBitmapLock_GetDataPointer_STA_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693719"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a><span data-ttu-id="ab2ac-103">Ивикбитмаплокк \_ жетдатапоинтер \_ STA \_ -функция</span><span class="sxs-lookup"><span data-stu-id="ab2ac-103">IWICBitmapLock\_GetDataPointer\_STA\_Proxy function</span></span>

<span data-ttu-id="ab2ac-104">Функция-посредник для метода [**жетдатапоинтер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .</span><span class="sxs-lookup"><span data-stu-id="ab2ac-104">Proxy function for the [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab2ac-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a><span data-ttu-id="ab2ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab2ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab2ac-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="ab2ac-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab2ac-108">Тип: \**[**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="ab2ac-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="ab2ac-109">Указатель на этот объект [_ *ивикбитмаплокк* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="ab2ac-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="ab2ac-110">*пкббуфферсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ab2ac-110">*pcbBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab2ac-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="ab2ac-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="ab2ac-112">Указатель, получающий размер буфера.</span><span class="sxs-lookup"><span data-stu-id="ab2ac-112">A pointer that receives the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ab2ac-113">_ppbData \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab2ac-113">_ppbData\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab2ac-114">Тип: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="ab2ac-114">Type: **BYTE\*\***</span></span>

<span data-ttu-id="ab2ac-115">Указатель, получающий указатель на верхний левый пиксель в заблокированном прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="ab2ac-115">A pointer that receives a pointer to the top left pixel in the locked rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab2ac-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab2ac-116">Return value</span></span>

<span data-ttu-id="ab2ac-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab2ac-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ab2ac-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ab2ac-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab2ac-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab2ac-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab2ac-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="ab2ac-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2ac-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ab2ac-121">Requirements</span></span>



| <span data-ttu-id="ab2ac-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ab2ac-122">Requirement</span></span> | <span data-ttu-id="ab2ac-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ab2ac-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2ac-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab2ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ab2ac-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab2ac-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ab2ac-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab2ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ab2ac-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab2ac-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ab2ac-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ab2ac-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab2ac-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab2ac-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




