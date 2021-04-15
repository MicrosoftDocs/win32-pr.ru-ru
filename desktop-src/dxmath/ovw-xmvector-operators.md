---
description: Структура КСМВЕКТОР представляет следующие операторы.
ms.assetid: 16fc1276-7bed-4e6f-8af5-d871afa73b68
title: Операторы КСМВЕКТОР
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0611be5e9737e2829bc06f9a3fade10db233cbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701867"
---
# <a name="xmvector-operators"></a><span data-ttu-id="07893-103">Операторы КСМВЕКТОР</span><span class="sxs-lookup"><span data-stu-id="07893-103">XMVECTOR Operators</span></span>

<span data-ttu-id="07893-104">Структура [**ксмвектор**](xmvector-data-type.md) представляет следующие операторы.</span><span class="sxs-lookup"><span data-stu-id="07893-104">The following operators are exposed by the [**XMVECTOR**](xmvector-data-type.md) structure.</span></span>

> [!Note]  
> <span data-ttu-id="07893-105">Указанные здесь операторы доступны только в C++.</span><span class="sxs-lookup"><span data-stu-id="07893-105">The operators listed here are only available under C++.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="07893-106">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="07893-106">In this section</span></span>



| <span data-ttu-id="07893-107">Методы</span><span class="sxs-lookup"><span data-stu-id="07893-107">Methods</span></span>                                                    | <span data-ttu-id="07893-108">Описание</span><span class="sxs-lookup"><span data-stu-id="07893-108">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07893-109">[**operator + =**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07893-109">[**operator +=**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span></span><br/>  | <span data-ttu-id="07893-110">Добавляет значение с плавающей запятой к `XMVECTOR` экземпляру и возвращает ссылку на обновленный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="07893-110">Adds a floating point value to an `XMVECTOR` instance, and returns a reference to the updated instance.</span></span> <br/>                         |
| <span data-ttu-id="07893-111">[**Оператор-=**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07893-111">[**operator -=**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span></span><br/>    | <span data-ttu-id="07893-112">Вычитает значение с плавающей запятой из текущего экземпляра `XMVECTOR` , возвращая результат в обновленном текущем экземпляре.</span><span class="sxs-lookup"><span data-stu-id="07893-112">Subtracts a floating point value from the current instance of `XMVECTOR`, returning the result in the updated current instance.</span></span> <br/> |
| [<span data-ttu-id="07893-113">\**оператор \** _</span><span class="sxs-lookup"><span data-stu-id="07893-113">\**operator \** _</span></span>](xmvector-operator-mul.md)<br/>    | <span data-ttu-id="07893-114">Операторы умножения</span><span class="sxs-lookup"><span data-stu-id="07893-114">Multiplication operators</span></span><br/>                                                                                                         |
| [<span data-ttu-id="07893-115">*оператор \* =* _\*</span><span class="sxs-lookup"><span data-stu-id="07893-115">_ *operator \*=*\*</span></span>](xmvector-operator-muleq.md)<br/> | <span data-ttu-id="07893-116">Операторы присваивания умножения</span><span class="sxs-lookup"><span data-stu-id="07893-116">Multiplication assignment operators</span></span><br/>                                                                                              |
| [<span data-ttu-id="07893-117">**станции**</span><span class="sxs-lookup"><span data-stu-id="07893-117">**operator /**</span></span>](xmvector-operator-div.md)<br/>     | <span data-ttu-id="07893-118">Оператор деления.</span><span class="sxs-lookup"><span data-stu-id="07893-118">Division operator.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="07893-119">**Оператор/=**</span><span class="sxs-lookup"><span data-stu-id="07893-119">**operator /=**</span></span>](xmvector-operator-diveq.md)<br/>  | <span data-ttu-id="07893-120">Оператор присваивания деления.</span><span class="sxs-lookup"><span data-stu-id="07893-120">Division Assignment operator.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="07893-121">**станции**</span><span class="sxs-lookup"><span data-stu-id="07893-121">**operator -**</span></span>](xmvector-operator--.md)<br/>       | <span data-ttu-id="07893-122">Вычитание и операторы отрицания</span><span class="sxs-lookup"><span data-stu-id="07893-122">Subtraction and negation operators</span></span><br/>                                                                                               |
| [<span data-ttu-id="07893-123">**operator +**</span><span class="sxs-lookup"><span data-stu-id="07893-123">**operator +**</span></span>](xmvector-operator-pls.md)<br/>     | <span data-ttu-id="07893-124">Операторы сложения.</span><span class="sxs-lookup"><span data-stu-id="07893-124">Addition operators.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="07893-125">См. также</span><span class="sxs-lookup"><span data-stu-id="07893-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07893-126">Расширения КСМВЕКТОР</span><span class="sxs-lookup"><span data-stu-id="07893-126">XMVECTOR Extensions</span></span>](ovw-xmvector-extensions.md)
</dt> <dt>

<span data-ttu-id="07893-127">**Типы**</span><span class="sxs-lookup"><span data-stu-id="07893-127">**Types**</span></span>
</dt> <dt>

[<span data-ttu-id="07893-128">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="07893-128">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
