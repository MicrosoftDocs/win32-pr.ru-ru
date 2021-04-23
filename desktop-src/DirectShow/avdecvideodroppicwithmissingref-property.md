---
description: Указывает, будет ли декодер удалять фреймы с отсутствующими опорными кадрами.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Свойство Авдеквидеодроппиквисмиссингреф (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262363"
---
# <a name="avdecvideodroppicwithmissingref-property"></a><span data-ttu-id="fe270-103">Авдеквидеодроппиквисмиссингреф, свойство</span><span class="sxs-lookup"><span data-stu-id="fe270-103">AVDecVideoDropPicWithMissingRef property</span></span>

<span data-ttu-id="fe270-104">Указывает, будет ли декодер удалять фреймы с отсутствующими опорными кадрами.</span><span class="sxs-lookup"><span data-stu-id="fe270-104">Specifies whether the decoder drops intra frames with missing reference frames.</span></span>

<span data-ttu-id="fe270-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="fe270-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe270-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fe270-106">Data type</span></span>

<span data-ttu-id="fe270-107">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="fe270-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fe270-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="fe270-108">Property GUID</span></span>

<span data-ttu-id="fe270-109">**КОДЕКАПИ \_ авдеквидеодроппиквисмиссингреф**</span><span class="sxs-lookup"><span data-stu-id="fe270-109">**CODECAPI\_AVDecVideoDropPicWithMissingRef**</span></span>

## <a name="remarks"></a><span data-ttu-id="fe270-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe270-110">Remarks</span></span>

<span data-ttu-id="fe270-111">Если битовый поток поврежден, в кадре могут отсутствовать кадры ссылок.</span><span class="sxs-lookup"><span data-stu-id="fe270-111">If the bitstream is corrupted, a frame might have missing reference frames.</span></span> <span data-ttu-id="fe270-112">Если это свойство имеет значение **Variant \_ true**, декодер удаляет кадр.</span><span class="sxs-lookup"><span data-stu-id="fe270-112">If the value of this property is **VARIANT\_TRUE**, the decoder drops the frame.</span></span> <span data-ttu-id="fe270-113">Если значение является **вариантным \_ false**, декодер пытается декодировать кадр, используя один или несколько ближайших кадров в качестве ссылочных кадров.</span><span class="sxs-lookup"><span data-stu-id="fe270-113">If the value is **VARIANT\_FALSE**, the decoder attempts to decode the frame, using one or more nearby frames as reference frames.</span></span> <span data-ttu-id="fe270-114">Результирующий декодированный кадр будет блокировать артефакты.</span><span class="sxs-lookup"><span data-stu-id="fe270-114">The resulting decoded frame will have blocking artifacts.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe270-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fe270-115">Requirements</span></span>



| <span data-ttu-id="fe270-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fe270-116">Requirement</span></span> | <span data-ttu-id="fe270-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fe270-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe270-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe270-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe270-119">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fe270-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fe270-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe270-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe270-121">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="fe270-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fe270-122">Header</span><span class="sxs-lookup"><span data-stu-id="fe270-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe270-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe270-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe270-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe270-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe270-125">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="fe270-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fe270-126">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="fe270-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




