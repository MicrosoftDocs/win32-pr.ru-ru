---
description: Поле Длина в TLV-tripletе определяет число байтов, закодированных в поле значение.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Закодированная Длина и байты значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662857"
---
# <a name="encoded-length-and-value-bytes"></a><span data-ttu-id="95144-103">Закодированная Длина и байты значений</span><span class="sxs-lookup"><span data-stu-id="95144-103">Encoded Length and Value Bytes</span></span>

<span data-ttu-id="95144-104">Поле *Длина* в TLV-tripletе определяет число байтов, закодированных в поле *значение* .</span><span class="sxs-lookup"><span data-stu-id="95144-104">The *Length* field in a TLV triplet identifies the number of bytes encoded in the *Value* field.</span></span> <span data-ttu-id="95144-105">Поле *значение* содержит содержимое, отправляемое между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="95144-105">The *Value* field contains the content being sent between computers.</span></span> <span data-ttu-id="95144-106">Если поле *значения* содержит менее 128 байт, в поле *Длина* необходимо указать только один байт.</span><span class="sxs-lookup"><span data-stu-id="95144-106">If the *Value* field contains fewer than 128 bytes, the *Length* field requires only one byte.</span></span> <span data-ttu-id="95144-107">Бит 7 поля *длины* равен нулю (0), а оставшийся бит определяет число байтов отправляемого содержимого.</span><span class="sxs-lookup"><span data-stu-id="95144-107">Bit 7 of the *Length* field is zero (0) and the remaining bits identify the number of bytes of content being sent.</span></span> <span data-ttu-id="95144-108">Если поле *значения* содержит более 127 байт, в поле *length* (1) используется бит 7, а остальные биты указывают количество байтов, необходимое для хранения длины.</span><span class="sxs-lookup"><span data-stu-id="95144-108">If the *Value* field contains more than 127 bytes, bit 7 of the *Length* field is one (1) and the remaining bits identify the number of bytes needed to contain the length.</span></span> <span data-ttu-id="95144-109">Примеры показаны на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="95144-109">Examples are shown in the following illustration.</span></span>

![байт TLV длиной der](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a><span data-ttu-id="95144-111">См. также</span><span class="sxs-lookup"><span data-stu-id="95144-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95144-112">Синтаксис преобразования DER</span><span class="sxs-lookup"><span data-stu-id="95144-112">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
</dt> <dt>

[<span data-ttu-id="95144-113">Байты закодированного тега</span><span class="sxs-lookup"><span data-stu-id="95144-113">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



