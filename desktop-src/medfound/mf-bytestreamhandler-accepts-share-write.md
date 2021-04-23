---
description: Указывает, может ли обработчик потока байтов использовать поток байтов, Открытый для записи другим потоком.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Атрибут MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683122"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a><span data-ttu-id="f2f47-103">MF \_ битестреамхандлер \_ принимает \_ \_ атрибут общей записи</span><span class="sxs-lookup"><span data-stu-id="f2f47-103">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute</span></span>

<span data-ttu-id="f2f47-104">Указывает, может ли обработчик потока байтов использовать поток байтов, Открытый для записи другим потоком.</span><span class="sxs-lookup"><span data-stu-id="f2f47-104">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread.</span></span>

## <a name="data-type"></a><span data-ttu-id="f2f47-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f2f47-105">Data type</span></span>

<span data-ttu-id="f2f47-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f2f47-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f2f47-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="f2f47-107">Get/set</span></span>

<span data-ttu-id="f2f47-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f2f47-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f2f47-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f2f47-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2f47-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2f47-110">Remarks</span></span>

<span data-ttu-id="f2f47-111">Обработчики потока байтов могут поддерживать этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="f2f47-111">Byte-stream handlers can support this attribute.</span></span> <span data-ttu-id="f2f47-112">Чтобы получить или задать атрибут, сначала запросите обработчик потока байтов для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="f2f47-112">To get or set the attribute, first query the byte-stream handler for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="f2f47-113">Затем вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) или [**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span><span class="sxs-lookup"><span data-stu-id="f2f47-113">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) or [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span></span>

<span data-ttu-id="f2f47-114">Если этот атрибут имеет **значение true**, это означает, что обработчик потока байтов может считывать данные из потока, в то время как другой поток выполняет запись в тот же поток.</span><span class="sxs-lookup"><span data-stu-id="f2f47-114">If this attribute is **TRUE**, it means that the byte-stream handler can read from a stream while another thread writes to the same stream.</span></span> <span data-ttu-id="f2f47-115">Когда поток открывается для записи другим потоком, метод [**имфбитестреам:: Capabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) Возвращает флаг **\_ \_ записи мфбитестреам Share** .</span><span class="sxs-lookup"><span data-stu-id="f2f47-115">When a stream is opened for writing by another thread, the [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) method returns the **MFBYTESTREAM\_SHARE\_WRITE** flag.</span></span>

<span data-ttu-id="f2f47-116">Этот атрибут влияет на разрешение исходного кода.</span><span class="sxs-lookup"><span data-stu-id="f2f47-116">This attribute affects source resolution.</span></span> <span data-ttu-id="f2f47-117">Если для потока байтов установлен флаг **\_ \_ записи общего ресурса мфбитестреам** , то [сопоставитель источника](source-resolver.md) не передаст поток в обработчик потока байтов, если только обработчик не имеет атрибут MF битестреамхандлер, \_ \_ принимающий \_ общий доступ \_ для записи. </span><span class="sxs-lookup"><span data-stu-id="f2f47-117">If a byte stream has the **MFBYTESTREAM\_SHARE\_WRITE** flag set, the [Source Resolver](source-resolver.md) will not pass that stream to a byte-stream handler unless the handler has the MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute set to **TRUE**.</span></span>

<span data-ttu-id="f2f47-118">Флаг **\_ \_ записи общего ресурса мфбитестреам** является указанием того, что длина потока может измениться во время чтения обработчика из него.</span><span class="sxs-lookup"><span data-stu-id="f2f47-118">The **MFBYTESTREAM\_SHARE\_WRITE** flag is a hint that the length of the stream might change while the handler is reading from it.</span></span>

<span data-ttu-id="f2f47-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="f2f47-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f47-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f2f47-120">Requirements</span></span>



| <span data-ttu-id="f2f47-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f2f47-121">Requirement</span></span> | <span data-ttu-id="f2f47-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f2f47-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f47-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2f47-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f47-124">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f2f47-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f2f47-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2f47-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f47-126">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f2f47-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f2f47-127">Header</span><span class="sxs-lookup"><span data-stu-id="f2f47-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f47-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f47-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f47-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2f47-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f47-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2f47-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2f47-131">Обработчики схем и обработчики Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="f2f47-131">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




