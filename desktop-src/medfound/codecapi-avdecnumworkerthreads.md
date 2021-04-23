---
description: Задает число рабочих потоков, используемых видеодекодером.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Свойство CODECAPI_AVDecNumWorkerThreads (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710844"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a><span data-ttu-id="6075c-103">КОДЕКАПИ \_ авдекнумворкерсреадс, свойство</span><span class="sxs-lookup"><span data-stu-id="6075c-103">CODECAPI\_AVDecNumWorkerThreads property</span></span>

<span data-ttu-id="6075c-104">Задает число рабочих потоков, используемых видеодекодером.</span><span class="sxs-lookup"><span data-stu-id="6075c-104">Sets the number of worker threads that are used by a video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="6075c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6075c-105">Data type</span></span>

<span data-ttu-id="6075c-106">**Long** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="6075c-106">**LONG** (**VT\_I4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6075c-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="6075c-107">Property GUID</span></span>

<span data-ttu-id="6075c-108">КОДЕКАПИ \_ авдекнумворкерсреадс</span><span class="sxs-lookup"><span data-stu-id="6075c-108">CODECAPI\_AVDecNumWorkerThreads</span></span>

## <a name="remarks"></a><span data-ttu-id="6075c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6075c-109">Remarks</span></span>

<span data-ttu-id="6075c-110">Если значение равно 1, декодер выбирает число потоков.</span><span class="sxs-lookup"><span data-stu-id="6075c-110">If the value is  1, the decoder selects the number of threads.</span></span>

<span data-ttu-id="6075c-111">Для интерфейса [**икодекапи**](/windows/desktop/api/strmif/nn-strmif-icodecapi) задайте для этого свойства значение **Long** (**VT \_ I4**).</span><span class="sxs-lookup"><span data-stu-id="6075c-111">For the [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) interface, set this property as a **LONG** value (**VT\_I4**).</span></span> <span data-ttu-id="6075c-112">Для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) установите это свойство как **UINT32**, хотя значение подписывается.</span><span class="sxs-lookup"><span data-stu-id="6075c-112">For the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, set this property as a **UINT32**, although the value is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6075c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6075c-113">Requirements</span></span>



| <span data-ttu-id="6075c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6075c-114">Requirement</span></span> | <span data-ttu-id="6075c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6075c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6075c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6075c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6075c-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="6075c-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="6075c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6075c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6075c-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="6075c-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6075c-120">Header</span><span class="sxs-lookup"><span data-stu-id="6075c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6075c-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6075c-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6075c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6075c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6075c-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6075c-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6075c-124">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="6075c-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

