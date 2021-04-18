---
description: В этом разделе приведены справочные спецификации для констант прямого управления.
ms.assetid: 41A828F5-4AE3-4073-89EB-CC1279B9ECED
title: Константы прямой манипуляции
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5040191f22e92dcfb8c2ca26edd4080cd4cbb2be
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105719240"
---
# <a name="direct-manipulation-constants"></a><span data-ttu-id="d9b6b-103">Константы прямой манипуляции</span><span class="sxs-lookup"><span data-stu-id="d9b6b-103">Direct Manipulation Constants</span></span>

<span data-ttu-id="d9b6b-104">В этом разделе приведены справочные спецификации для констант [прямого управления](direct-manipulation-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b6b-104">This section provides the reference specifications for [Direct Manipulation](direct-manipulation-portal.md) constants.</span></span>

| <span data-ttu-id="d9b6b-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="d9b6b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="d9b6b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d9b6b-106">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span id="DIRECTMANIPULATION_KEYBOARDFOCUS"></span><span id="directmanipulation_keyboardfocus"></span><dl> <span data-ttu-id="d9b6b-107"><dt>**Директманипулатион \_ КЭЙБОАРДФОКУС**</dt> <dt>0xFFFFFFFE</dt></span><span class="sxs-lookup"><span data-stu-id="d9b6b-107"><dt>**DIRECTMANIPULATION\_KEYBOARDFOCUS**</dt> <dt>0xFFFFFFFE</dt></span></span> </dl> | <span data-ttu-id="d9b6b-108">Указывает идентификатор псуедо-указателя для эмуляции сенсорного контакта с помощью ввода с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="d9b6b-108">Specifies a psuedo-pointer ID for emulating a touch contact through keyboard input.</span></span><br/> |
| <span id="DIRECTMANIPULATION_MOUSEFOCUS"></span><span id="directmanipulation_mousefocus"></span><dl> <span data-ttu-id="d9b6b-109"><dt>**Директманипулатион \_ МАУСЕФОКУС**</dt> <dt>0xFFFFFFFD</dt></span><span class="sxs-lookup"><span data-stu-id="d9b6b-109"><dt>**DIRECTMANIPULATION\_MOUSEFOCUS**</dt> <dt>0xFFFFFFFD</dt></span></span> </dl>          | <span data-ttu-id="d9b6b-110">Указывает идентификатор псуедо-указателя для эмуляции сенсорного контакта с помощью ввода мыши.</span><span class="sxs-lookup"><span data-stu-id="d9b6b-110">Specifies a psuedo-pointer ID for emulating a touch contact through mouse input.</span></span><br/>    |
| <span id="DIRECTMANIPULATION_MINIMUM_ZOOM"></span><span id="directmanipulation_minimum_zoom"></span><dl> <span data-ttu-id="d9b6b-111"><dt>**Директманипулатион \_ Минимальный \_ масштаб**</dt> <dt>0,1</dt></span><span class="sxs-lookup"><span data-stu-id="d9b6b-111"><dt>**DIRECTMANIPULATION\_MINIMUM\_ZOOM**</dt> <dt>0.1</dt></span></span> </dl>          | <span data-ttu-id="d9b6b-112">Указывает минимально допустимую границу масштабирования, равное 10%.</span><span class="sxs-lookup"><span data-stu-id="d9b6b-112">Specifies the minimum permitted zoom boundary of 10%.</span></span><br/>                               |

## <a name="requirements"></a><span data-ttu-id="d9b6b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d9b6b-113">Requirements</span></span>

| <span data-ttu-id="d9b6b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d9b6b-114">Requirement</span></span> | <span data-ttu-id="d9b6b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d9b6b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b6b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9b6b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b6b-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d9b6b-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="d9b6b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9b6b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b6b-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d9b6b-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d9b6b-120">IDL</span><span class="sxs-lookup"><span data-stu-id="d9b6b-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d9b6b-121"><dt>Директманипулатион. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9b6b-121"><dt>DirectManipulation.idl</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d9b6b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9b6b-122">See also</span></span>

[<span data-ttu-id="d9b6b-123">Ссылка на прямую манипуляцию</span><span class="sxs-lookup"><span data-stu-id="d9b6b-123">Direct Manipulation Reference</span></span>](direct-manipulation-reference.md)
