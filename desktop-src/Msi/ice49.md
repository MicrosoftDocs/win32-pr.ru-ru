---
description: ICE49 проверяет наличие записей реестра по умолчанию, которые не являются \_ типом reg SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911912"
---
# <a name="ice49"></a><span data-ttu-id="335b4-103">ICE49</span><span class="sxs-lookup"><span data-stu-id="335b4-103">ICE49</span></span>

<span data-ttu-id="335b4-104">ICE49 проверяет наличие записей реестра по умолчанию, которые не являются типом **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="335b4-104">ICE49 checks for default registry entries that are not a **REG\_SZ** type.</span></span>

## <a name="result"></a><span data-ttu-id="335b4-105">Результат</span><span class="sxs-lookup"><span data-stu-id="335b4-105">Result</span></span>

<span data-ttu-id="335b4-106">ICE49 отправляет предупреждение, если имеется запись реестра по умолчанию, которая не является типом **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="335b4-106">ICE49 posts an warning if there is a default registry entry that is not a **REG\_SZ** type.</span></span>

## <a name="example"></a><span data-ttu-id="335b4-107">Пример</span><span class="sxs-lookup"><span data-stu-id="335b4-107">Example</span></span>

<span data-ttu-id="335b4-108">ICE49 сообщает следующее предупреждение для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="335b4-108">ICE49 reports the following warning for the example shown.</span></span>

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

<span data-ttu-id="335b4-109">Значение " \# 123" является значением реестра **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="335b4-109">The value '\#123' is a **DWORD** registry value.</span></span>

<span data-ttu-id="335b4-110">[Таблица реестра](registry-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="335b4-110">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="335b4-111">Реестр</span><span class="sxs-lookup"><span data-stu-id="335b4-111">Registry</span></span> | <span data-ttu-id="335b4-112">Имя</span><span class="sxs-lookup"><span data-stu-id="335b4-112">Name</span></span> | <span data-ttu-id="335b4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="335b4-113">Value</span></span> |
|----------|------|-------|
| <span data-ttu-id="335b4-114">Reg1</span><span class="sxs-lookup"><span data-stu-id="335b4-114">Reg1</span></span>     |      | <span data-ttu-id="335b4-115">\#123</span><span class="sxs-lookup"><span data-stu-id="335b4-115">\#123</span></span> |



 

<span data-ttu-id="335b4-116">Чтобы устранить это предупреждение, измените значение на введите **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="335b4-116">To fix this warning, change the value to type **REG\_SZ**.</span></span>

<span data-ttu-id="335b4-117">Компоненты с **\_ SZами** , отличными от reg, являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="335b4-117">Components with non-**REG\_SZ** are valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="335b4-118">См. также</span><span class="sxs-lookup"><span data-stu-id="335b4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="335b4-119">Синтаксис условных операторов</span><span class="sxs-lookup"><span data-stu-id="335b4-119">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="335b4-120">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="335b4-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



