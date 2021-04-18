---
description: Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Свойство MFPKEY_CODEDNONZEROFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711943"
---
# <a name="mfpkey_codednonzeroframes-property"></a><span data-ttu-id="6415b-103">МФПКЭЙ \_ кодеднонзерофрамес, свойство</span><span class="sxs-lookup"><span data-stu-id="6415b-103">MFPKEY\_CODEDNONZEROFRAMES Property</span></span>

<span data-ttu-id="6415b-104">Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.</span><span class="sxs-lookup"><span data-stu-id="6415b-104">Specifies the number of video frames encoded by the codec that actually contain data.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6415b-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="6415b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="6415b-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="6415b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="6415b-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6415b-107">Data Type</span></span>

<span data-ttu-id="6415b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6415b-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="6415b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6415b-109">Remarks</span></span>

<span data-ttu-id="6415b-110">Это значение равно [мфпкэй \_ тоталфрамес](mfpkey-totalframesproperty.md) минус все кадры, которые были удалены из-за ограничений битовой частоты, за вычетом кадров нулевых байтов.</span><span class="sxs-lookup"><span data-stu-id="6415b-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints, minus any zero-byte frames.</span></span> <span data-ttu-id="6415b-111">Это значение можно получить после завершения передачи образцов.</span><span class="sxs-lookup"><span data-stu-id="6415b-111">You can get this value after you are finished passing samples.</span></span> <span data-ttu-id="6415b-112">Для повторяющихся кадров можно создавать кадры нулевого байта.</span><span class="sxs-lookup"><span data-stu-id="6415b-112">Zero-byte frames can be created for duplicate frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="6415b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6415b-113">Requirements</span></span>



| <span data-ttu-id="6415b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6415b-114">Requirement</span></span> | <span data-ttu-id="6415b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6415b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6415b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6415b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6415b-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6415b-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6415b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6415b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6415b-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6415b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6415b-120">Header</span><span class="sxs-lookup"><span data-stu-id="6415b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6415b-121"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6415b-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6415b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6415b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6415b-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6415b-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
