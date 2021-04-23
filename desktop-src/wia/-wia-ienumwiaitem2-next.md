---
description: Заполняет массив указателей на интерфейсы IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'Метод IEnumWiaItem2:: Next (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263314"
---
# <a name="ienumwiaitem2next-method"></a><span data-ttu-id="b5839-103">Метод IEnumWiaItem2:: Next</span><span class="sxs-lookup"><span data-stu-id="b5839-103">IEnumWiaItem2::Next method</span></span>

<span data-ttu-id="b5839-104">Заполняет массив указателей на интерфейсы [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="b5839-104">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5839-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5839-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b5839-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5839-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5839-107">*cElt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5839-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5839-108">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="b5839-108">Type: **ULONG**</span></span>

<span data-ttu-id="b5839-109">Указывает количество элементов массива в массиве, указанное параметром *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="b5839-109">Specifies the number of array elements in the array indicated by the *ppIWiaItem2* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b5839-110">*ppIWiaItem2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b5839-110">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5839-111">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b5839-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="b5839-112">Получает адрес массива указателей интерфейса [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="b5839-112">Receives the address of an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers.</span></span> <span data-ttu-id="b5839-113">**IEnumWiaItem2:: Next** заполняет этот массив указателями интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b5839-113">**IEnumWiaItem2::Next** fills this array with interface pointers.</span></span>

</dd> <dt>

<span data-ttu-id="b5839-114">*пцелтфетчед* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b5839-114">*pcEltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5839-115">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="b5839-115">Type: \**ULONG\** _</span></span>

<span data-ttu-id="b5839-116">На выходе этот параметр получает число указателей интерфейса, которые фактически хранятся в массиве, указанном параметром _ppIWiaItem2 \*.</span><span class="sxs-lookup"><span data-stu-id="b5839-116">On output, this parameter receives the number of interface pointers actually stored in the array indicated by the _ppIWiaItem2\* parameter.</span></span> <span data-ttu-id="b5839-117">По завершении перечисления этот параметр содержит нуль.</span><span class="sxs-lookup"><span data-stu-id="b5839-117">When the enumeration is complete, this parameter contains zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5839-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5839-118">Return value</span></span>

<span data-ttu-id="b5839-119">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b5839-119">Type: **HRESULT**</span></span>

<span data-ttu-id="b5839-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b5839-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5839-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5839-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5839-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5839-122">Remarks</span></span>

<span data-ttu-id="b5839-123">Система времени выполнения Windows Image (WIA) 2,0 представляет устройство WIA 2,0 как иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="b5839-123">The Windows Image Acquisition (WIA) 2.0 run-time system represents WIA 2.0 hardware devices as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="b5839-124">Приложения используют метод **IEnumWiaItem2:: Next** для получения указателя на интерфейс **IWiaItem2** для каждого элемента в текущей папке в дереве объектов **IWiaItem2** аппаратного устройства.</span><span class="sxs-lookup"><span data-stu-id="b5839-124">Applications use the **IEnumWiaItem2::Next** method to obtain an **IWiaItem2** interface pointer for each item in the current folder of a hardware device's **IWiaItem2** object tree.</span></span>

<span data-ttu-id="b5839-125">Чтобы получить список указателей, приложение передает массив [**IWiaItem2ных**](-wia-iwiaitem2.md) указателей интерфейса, которые он выделяет.</span><span class="sxs-lookup"><span data-stu-id="b5839-125">To obtain the list of pointers, the application passes an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers that it allocates.</span></span> <span data-ttu-id="b5839-126">Он также передает количество элементов массива в параметре *cElt*.</span><span class="sxs-lookup"><span data-stu-id="b5839-126">It also passes the number of array elements in the parameter *cElt*.</span></span> <span data-ttu-id="b5839-127">Метод **IEnumWiaItem2:: Next** заполняет массив указателями на интерфейсы **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="b5839-127">The **IEnumWiaItem2::Next** method fills the array with pointers to **IWiaItem2** interfaces.</span></span>

<span data-ttu-id="b5839-128">До завершения процесса перечисления метод **IEnumWiaItem2:: Next** возвращает значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b5839-128">Until the enumeration process completes, the **IEnumWiaItem2::Next** method returns S\_OK.</span></span> <span data-ttu-id="b5839-129">Каждый раз он устанавливает значение, на которое указывает, *пцелтфетчед* число элементов, вставляемых в массив.</span><span class="sxs-lookup"><span data-stu-id="b5839-129">Each time it does, it sets the value pointed to by *pcEltFetched* to the number of items it inserted into the array.</span></span> <span data-ttu-id="b5839-130">Когда **IEnumWiaItem2:: Next** завершает процесс перечисления объектов [**IWiaItem2**](-wia-iwiaitem2.md) , он возвращает \_ значение false и задает для расположения памяти, на которое указывает *пцелтфетчед* , значение 0.</span><span class="sxs-lookup"><span data-stu-id="b5839-130">When **IEnumWiaItem2::Next** finishes the process of enumerating [**IWiaItem2**](-wia-iwiaitem2.md) objects, it returns S\_FALSE and sets the memory location pointed to by *pcEltFetched* to zero.</span></span>

<span data-ttu-id="b5839-131">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="b5839-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5839-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b5839-132">Requirements</span></span>



| <span data-ttu-id="b5839-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b5839-133">Requirement</span></span> | <span data-ttu-id="b5839-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b5839-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5839-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5839-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b5839-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5839-136">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b5839-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5839-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b5839-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5839-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5839-139">Header</span><span class="sxs-lookup"><span data-stu-id="b5839-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5839-140"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5839-140"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5839-141">IDL</span><span class="sxs-lookup"><span data-stu-id="b5839-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5839-142"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5839-142"><dt>Wia.idl</dt></span></span> </dl> |



 

 
