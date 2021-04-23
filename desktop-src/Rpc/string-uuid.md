---
title: Строковый UUID
description: Строковый идентификатор UUID содержит представление символьного массива UUID.
ms.assetid: a8a04c88-0d41-4e0c-aae1-caa6c95f91c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6e9aae4e1fb8a2878388f042bc1e5b2f0d45a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987787"
---
# <a name="string-uuid"></a><span data-ttu-id="ef55f-103">Строковый UUID</span><span class="sxs-lookup"><span data-stu-id="ef55f-103">String UUID</span></span>

<span data-ttu-id="ef55f-104">Строковый идентификатор UUID содержит представление символьного массива UUID.</span><span class="sxs-lookup"><span data-stu-id="ef55f-104">A string UUID contains the character-array representation of a UUID.</span></span> <span data-ttu-id="ef55f-105">Строковый идентификатор UUID состоит из нескольких полей шестнадцатеричных символов.</span><span class="sxs-lookup"><span data-stu-id="ef55f-105">A string UUID is composed of multiple fields of hexadecimal characters.</span></span> <span data-ttu-id="ef55f-106">Каждый элемент имеет фиксированную длину, а поля разделяются символом дефиса.</span><span class="sxs-lookup"><span data-stu-id="ef55f-106">Each member has a fixed length, and fields are separated by the hyphen character.</span></span> <span data-ttu-id="ef55f-107">Пример:</span><span class="sxs-lookup"><span data-stu-id="ef55f-107">For example:</span></span>

`989C6E5C-2CC1-11CA-A044-08002B1BB4F5`

<span data-ttu-id="ef55f-108">При предоставлении строкового UUID в качестве входного параметра для функции времени выполнения RPC введите шестнадцатеричные символы алфавита как в верхнем, так и в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="ef55f-108">When providing a string UUID as an input parameter to an RPC run-time function, enter the alphabetic hexadecimal characters as either uppercase or lowercase characters.</span></span> <span data-ttu-id="ef55f-109">Однако если функция времени выполнения возвращает строковый идентификатор, шестнадцатеричные символы всегда являются строчными.</span><span class="sxs-lookup"><span data-stu-id="ef55f-109">However, when a run-time function returns a string UUID, the hexadecimal characters are always lowercase.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef55f-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ef55f-110">Related topics</span></span>

<dl> <span data-ttu-id="ef55f-111"><dt>
[**UUID**](./rpcdce/ns-rpcdce-uuid.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="ef55f-111"><dt>
[**UUID**](./rpcdce/ns-rpcdce-uuid.md)
</dt> </span></span></dl>

 

 