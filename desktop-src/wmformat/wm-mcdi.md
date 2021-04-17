---
title: WM/МКДИ
description: Атрибут WM/МКДИ содержит идентификатор музыкального компакт-диска. Это двоичный дамп оглавления с компакт-диска, который используется для уникальной идентификации компакт-диска.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Формат Windows Media WM/МКДИ
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105710203"
---
# <a name="wmmcdi"></a><span data-ttu-id="7b1e8-105">WM/МКДИ</span><span class="sxs-lookup"><span data-stu-id="7b1e8-105">WM/MCDI</span></span>

<span data-ttu-id="7b1e8-106">Атрибут **WM/мкди** содержит идентификатор музыкального компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7b1e8-106">The **WM/MCDI** attribute contains the music CD identifier.</span></span> <span data-ttu-id="7b1e8-107">Это двоичный дамп оглавления с компакт-диска, который используется для уникальной идентификации компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7b1e8-107">This is a binary dump of the table of contents from the CD that is used to uniquely identify the CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7b1e8-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="7b1e8-108">Global Constant</span></span>

<span data-ttu-id="7b1e8-109">g \_ всзвммкди</span><span class="sxs-lookup"><span data-stu-id="7b1e8-109">g\_wszWMMCDI</span></span>

## <a name="data-type"></a><span data-ttu-id="7b1e8-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7b1e8-110">Data Type</span></span>

<span data-ttu-id="7b1e8-111">**\_ \_ двоичный тип ВМТ**</span><span class="sxs-lookup"><span data-stu-id="7b1e8-111">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="7b1e8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b1e8-112">Remarks</span></span>

<span data-ttu-id="7b1e8-113">Этот атрибут совместим с кадром ID3, МКДИ.</span><span class="sxs-lookup"><span data-stu-id="7b1e8-113">This attribute is compatible with the ID3 frame, MCDI.</span></span> <span data-ttu-id="7b1e8-114">Для спецификации ID3 для кадра МКДИ требуется, чтобы для каждого файла существовала только одна такая рамка, а также существовала допустимая ТРКК рамка.</span><span class="sxs-lookup"><span data-stu-id="7b1e8-114">The ID3 specification for the MCDI frame requires that only one such frame exist per file and that a valid TRCK frame exist.</span></span> <span data-ttu-id="7b1e8-115">Редактор метаданных не выполняет никаких проверок для этих правил.</span><span class="sxs-lookup"><span data-stu-id="7b1e8-115">The metadata editor does not perform any validation for these rules.</span></span> <span data-ttu-id="7b1e8-116">Кроме того, размер WM/МКДИ не ограничен 804 байтами, как и кадр МКДИ ID3.</span><span class="sxs-lookup"><span data-stu-id="7b1e8-116">Also, the size of WM/MCDI is not limited to 804 bytes, as is the MCDI ID3 frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b1e8-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b1e8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1e8-118">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="7b1e8-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




