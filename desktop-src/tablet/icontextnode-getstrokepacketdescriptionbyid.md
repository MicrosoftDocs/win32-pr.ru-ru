---
description: Извлекает массив, содержащий идентификаторы свойств пакета для указанного росчерка.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Метод Иконтекстноде:: Жетстрокепаккетдескриптионбид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692443"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a><span data-ttu-id="4e323-103">Метод Иконтекстноде:: Жетстрокепаккетдескриптионбид</span><span class="sxs-lookup"><span data-stu-id="4e323-103">IContextNode::GetStrokePacketDescriptionById method</span></span>

<span data-ttu-id="4e323-104">Извлекает массив, содержащий идентификаторы свойств пакета для указанного росчерка.</span><span class="sxs-lookup"><span data-stu-id="4e323-104">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e323-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e323-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a><span data-ttu-id="4e323-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e323-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e323-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e323-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e323-108">Идентификатор для штриха.</span><span class="sxs-lookup"><span data-stu-id="4e323-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="4e323-109">*пулстрокепаккетдескриптионкаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4e323-109">*pulStrokePacketDescriptionCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e323-110">Число свойств пакетов в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="4e323-110">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="4e323-111">*ппстрокепаккетдескриптионгуидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4e323-111">*ppStrokePacketDescriptionGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e323-112">Массив, содержащий идентификаторы свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="4e323-112">An array containing the packet property identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e323-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e323-113">Return value</span></span>

<span data-ttu-id="4e323-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4e323-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e323-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e323-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4e323-116">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппстрокепаккетдескриптионгуидс* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="4e323-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppStrokePacketDescriptionGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="4e323-117">\**ппстрокепаккетдескриптионгуидс* содержит глобальные уникальные идентификаторы (GUID), которые описывают типы данных пакетов, включаемые для каждой точки в штрихе.</span><span class="sxs-lookup"><span data-stu-id="4e323-117">\**ppStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="4e323-118">Полный список доступных свойств пакетов см. в разделе [константы паккетпропертигуидс](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4e323-118">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e323-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4e323-119">Requirements</span></span>



| <span data-ttu-id="4e323-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4e323-120">Requirement</span></span> | <span data-ttu-id="4e323-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4e323-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e323-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e323-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4e323-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4e323-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4e323-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e323-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4e323-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e323-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4e323-126">Header</span><span class="sxs-lookup"><span data-stu-id="4e323-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e323-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4e323-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4e323-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4e323-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e323-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e323-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4e323-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e323-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e323-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="4e323-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4e323-132">**Иконтекстноде:: Жетстрокепаккетдатабид**</span><span class="sxs-lookup"><span data-stu-id="4e323-132">**IContextNode::GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[<span data-ttu-id="4e323-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="4e323-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

