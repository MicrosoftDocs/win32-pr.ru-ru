---
description: Извлекает массив, содержащий данные свойства пакета для указанного штриха.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Метод Иконтекстноде:: Жетстрокепаккетдатабид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692444"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a><span data-ttu-id="53004-103">Метод Иконтекстноде:: Жетстрокепаккетдатабид</span><span class="sxs-lookup"><span data-stu-id="53004-103">IContextNode::GetStrokePacketDataById method</span></span>

<span data-ttu-id="53004-104">Извлекает массив, содержащий данные свойства пакета для указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="53004-104">Retrieves an array containing the packet property data for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="53004-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53004-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="53004-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53004-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53004-107">*строкеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53004-107">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53004-108">Идентификатор для штриха.</span><span class="sxs-lookup"><span data-stu-id="53004-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="53004-109">*пстрокепаккетдатакаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="53004-109">*pStrokePacketDataCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53004-110">Длина массива данных пакета.</span><span class="sxs-lookup"><span data-stu-id="53004-110">The length of the packet data array.</span></span>

</dd> <dt>

<span data-ttu-id="53004-111">*пплстрокепаккетдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53004-111">*pplStrokePacketData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53004-112">Указатель на данные пакета для штриха.</span><span class="sxs-lookup"><span data-stu-id="53004-112">A pointer to the packet data for the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53004-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53004-113">Return value</span></span>

<span data-ttu-id="53004-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="53004-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="53004-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53004-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="53004-116">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *пплстрокепаккетдата* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="53004-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokePacketData* when you no longer need the information.</span></span>

 

<span data-ttu-id="53004-117">*плстрокепаккетдата* содержит данные пакетов для всех точек в штрихе.</span><span class="sxs-lookup"><span data-stu-id="53004-117">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="53004-118">Чтобы получить типы данных пакетов, включаемые для каждой точки в штрихе, используйте [**иконтекстноде:: жетстрокепаккетдескриптионбид**](icontextnode-getstrokepacketdescriptionbyid.md).</span><span class="sxs-lookup"><span data-stu-id="53004-118">To get the types of packet data included for each point in the stroke, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53004-119">Требования</span><span class="sxs-lookup"><span data-stu-id="53004-119">Requirements</span></span>



| <span data-ttu-id="53004-120">Требование</span><span class="sxs-lookup"><span data-stu-id="53004-120">Requirement</span></span> | <span data-ttu-id="53004-121">Значение</span><span class="sxs-lookup"><span data-stu-id="53004-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53004-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53004-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53004-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="53004-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53004-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53004-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53004-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="53004-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="53004-126">Header</span><span class="sxs-lookup"><span data-stu-id="53004-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="53004-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="53004-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="53004-128">DLL</span><span class="sxs-lookup"><span data-stu-id="53004-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53004-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53004-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="53004-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53004-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53004-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="53004-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="53004-132">**Иконтекстноде:: Жетстрокепаккетдескриптионбид**</span><span class="sxs-lookup"><span data-stu-id="53004-132">**IContextNode::GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[<span data-ttu-id="53004-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="53004-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

