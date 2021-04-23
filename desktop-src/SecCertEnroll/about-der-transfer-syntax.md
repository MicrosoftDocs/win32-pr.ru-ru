---
description: Применение правила кодирования к структурам данных, описанным в абстрактном синтаксисе, обеспечивает синтаксис передачи, который управляет тем, как байты в потоке упорядочиваются при передаче между компьютерами.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Синтаксис преобразования DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553937"
---
# <a name="der-transfer-syntax"></a><span data-ttu-id="71429-103">Синтаксис преобразования DER</span><span class="sxs-lookup"><span data-stu-id="71429-103">DER Transfer Syntax</span></span>

<span data-ttu-id="71429-104">Применение правила кодирования к структурам данных, описанным в абстрактном синтаксисе, обеспечивает синтаксис передачи, который управляет тем, как байты в потоке упорядочиваются при передаче между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="71429-104">Applying an encoding rule to the data structures described by an abstract syntax provides a transfer syntax that governs how bytes in a stream are organized when sent between computers.</span></span> <span data-ttu-id="71429-105">Синтаксис перемещения, используемый Distinguished Encoding Rules всегда соответствует *тегу, длине и* формату значения.</span><span class="sxs-lookup"><span data-stu-id="71429-105">The transfer syntax used by Distinguished Encoding Rules always follows a *Tag, Length, Value* format.</span></span> <span data-ttu-id="71429-106">Формат обычно называется TLV-Triplet, в котором каждое поле (T, L или V) содержит один или несколько байтов.</span><span class="sxs-lookup"><span data-stu-id="71429-106">The format is usually referred to as a TLV triplet in which each field (T, L, or V) contains one or more bytes.</span></span>

![Тип der, Длина и значение (TLV) Triplet](images/der-tlv-basic.png)

<span data-ttu-id="71429-108">Поле *Tag* указывает тип отправляемой структуры данных, поле *Длина* указывает число байтов передаваемого содержимого, а поле *значение* содержит содержимое.</span><span class="sxs-lookup"><span data-stu-id="71429-108">The *Tag* field specifies the type of the data structure being sent, the *Length* field specifies the number of bytes of content being transferred, and the *Value* field contains the content.</span></span> <span data-ttu-id="71429-109">Обратите внимание, что поле *value* может быть Triplet, если оно содержит сконструированный тип данных, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="71429-109">Note that the *Value* field can be a triplet if it contains a constructed data type as shown by the following illustration.</span></span>

![tripletная рекурсия der](images/der-tlv-recursive.png)

<span data-ttu-id="71429-111">Подробные сведения о компонентах TLV Triplet см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="71429-111">See the following topics for detailed information about the components of a TLV triplet.</span></span>

-   [<span data-ttu-id="71429-112">Байты закодированного тега</span><span class="sxs-lookup"><span data-stu-id="71429-112">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
-   [<span data-ttu-id="71429-113">Закодированная Длина и байты значений</span><span class="sxs-lookup"><span data-stu-id="71429-113">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a><span data-ttu-id="71429-114">См. также</span><span class="sxs-lookup"><span data-stu-id="71429-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71429-115">Сконструированные типы</span><span class="sxs-lookup"><span data-stu-id="71429-115">Constructed Types</span></span>](about-constructed-types.md)
</dt> <dt>

[<span data-ttu-id="71429-116">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="71429-116">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 



