---
description: Указывает, следует ли добавить в заголовок кадра циклическую проверку избыточности (CRC). Это свойство применяется к кодировщикам аудио в формате MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Свойство Авенкмпаенаблередунданципротектион (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655593"
---
# <a name="avencmpaenableredundancyprotection-property"></a><span data-ttu-id="c5ff7-104">Авенкмпаенаблередунданципротектион, свойство</span><span class="sxs-lookup"><span data-stu-id="c5ff7-104">AVEncMPAEnableRedundancyProtection property</span></span>

<span data-ttu-id="c5ff7-105">Указывает, следует ли добавить в заголовок кадра циклическую проверку избыточности (CRC).</span><span class="sxs-lookup"><span data-stu-id="c5ff7-105">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span> <span data-ttu-id="c5ff7-106">Это свойство применяется к кодировщикам аудио в формате MPEG.</span><span class="sxs-lookup"><span data-stu-id="c5ff7-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="c5ff7-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c5ff7-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c5ff7-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c5ff7-108">Data type</span></span>

<span data-ttu-id="c5ff7-109">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="c5ff7-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c5ff7-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="c5ff7-110">Property GUID</span></span>

<span data-ttu-id="c5ff7-111">**КОДЕКАПИ \_ авенкмпаенаблередунданципротектион**</span><span class="sxs-lookup"><span data-stu-id="c5ff7-111">**CODECAPI\_AVEncMPAEnableRedundancyProtection**</span></span>

## <a name="property-value"></a><span data-ttu-id="c5ff7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5ff7-112">Property value</span></span>

<span data-ttu-id="c5ff7-113">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c5ff7-113">This property can have the following values.</span></span>



| <span data-ttu-id="c5ff7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ff7-114">Value</span></span>          | <span data-ttu-id="c5ff7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c5ff7-115">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="c5ff7-116">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="c5ff7-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="c5ff7-117">Не добавляйте контрольную сумму CRC.</span><span class="sxs-lookup"><span data-stu-id="c5ff7-117">Do not add a CRC checksum.</span></span> |
| <span data-ttu-id="c5ff7-118">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="c5ff7-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="c5ff7-119">Добавление контрольной суммы CRC.</span><span class="sxs-lookup"><span data-stu-id="c5ff7-119">Add a CRC checksum.</span></span>        |



 

## <a name="requirements"></a><span data-ttu-id="c5ff7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ff7-120">Requirements</span></span>



| <span data-ttu-id="c5ff7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ff7-121">Requirement</span></span> | <span data-ttu-id="c5ff7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ff7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ff7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5ff7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ff7-124">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c5ff7-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c5ff7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5ff7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ff7-126">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="c5ff7-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c5ff7-127">Header</span><span class="sxs-lookup"><span data-stu-id="c5ff7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ff7-128"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff7-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ff7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5ff7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ff7-130">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="c5ff7-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c5ff7-131">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="c5ff7-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




