---
description: ICE79 проверяет ссылки на компоненты и компоненты, введенные в поля базы данных с помощью типа данных Condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154811"
---
# <a name="ice79"></a><span data-ttu-id="c29fd-103">ICE79</span><span class="sxs-lookup"><span data-stu-id="c29fd-103">ICE79</span></span>

<span data-ttu-id="c29fd-104">ICE79 проверяет ссылки на компоненты и компоненты, введенные в поля базы данных с помощью типа данных [Condition](condition.md) .</span><span class="sxs-lookup"><span data-stu-id="c29fd-104">ICE79 validates the references to components and features entered in the database fields using the [Condition](condition.md) data type.</span></span>

## <a name="result"></a><span data-ttu-id="c29fd-105">Результат</span><span class="sxs-lookup"><span data-stu-id="c29fd-105">Result</span></span>

<span data-ttu-id="c29fd-106">ICE79 отправляет два предупреждения.</span><span class="sxs-lookup"><span data-stu-id="c29fd-106">ICE79 posts two warnings.</span></span>



| <span data-ttu-id="c29fd-107">Предупреждение ICE79</span><span class="sxs-lookup"><span data-stu-id="c29fd-107">ICE79 warning</span></span>                                                                      | <span data-ttu-id="c29fd-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c29fd-108">Description</span></span>                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c29fd-109">В базе данных отсутствует \_ Таблица проверки.</span><span class="sxs-lookup"><span data-stu-id="c29fd-109">Database is missing \_Validation table.</span></span> <span data-ttu-id="c29fd-110">Не удалось полностью проверить имена свойств.</span><span class="sxs-lookup"><span data-stu-id="c29fd-110">Could not completely check property names.</span></span> | <span data-ttu-id="c29fd-111">В базе данных отсутствует [ \_ Таблица проверки](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="c29fd-111">Database is missing [\_Validation table](-validation-table.md).</span></span> |
| <span data-ttu-id="c29fd-112">Ошибка при получении значений из столбца \[ 2 \] в таблице \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="c29fd-112">Error retrieving values from column \[2\] in table \[1\].</span></span> <span data-ttu-id="c29fd-113">Пропуск столбца.</span><span class="sxs-lookup"><span data-stu-id="c29fd-113">Skipping Column.</span></span>         | <span data-ttu-id="c29fd-114">Ошибка при извлечении значения.</span><span class="sxs-lookup"><span data-stu-id="c29fd-114">Error retrieving value.</span></span>                                          |



 

<span data-ttu-id="c29fd-115">ICE79 отправляет две ошибки.</span><span class="sxs-lookup"><span data-stu-id="c29fd-115">ICE79 posts two errors.</span></span>



| <span data-ttu-id="c29fd-116">ICE79, ошибка</span><span class="sxs-lookup"><span data-stu-id="c29fd-116">ICE79 error</span></span>                                                          | <span data-ttu-id="c29fd-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c29fd-117">Description</span></span>                               |
|----------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c29fd-118">Компонент "% ls", указанный в столбце "% s". % s "строки% s является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="c29fd-118">Component '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span> | <span data-ttu-id="c29fd-119">Обнаружена недопустимая ссылка на компонент.</span><span class="sxs-lookup"><span data-stu-id="c29fd-119">An invalid component reference was found.</span></span> |
| <span data-ttu-id="c29fd-120">Компонент "% ls", указанный в столбце "% s". % s "строки% s является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="c29fd-120">Feature '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span>   | <span data-ttu-id="c29fd-121">Обнаружена недопустимая ссылка на компонент</span><span class="sxs-lookup"><span data-stu-id="c29fd-121">An invalid feature reference was found</span></span>    |



 

## <a name="example"></a><span data-ttu-id="c29fd-122">Пример</span><span class="sxs-lookup"><span data-stu-id="c29fd-122">Example</span></span>

<span data-ttu-id="c29fd-123">ICE79 сообщает о следующих ошибках в примере:</span><span class="sxs-lookup"><span data-stu-id="c29fd-123">ICE79 reports the following errors for the example:</span></span>

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

<span data-ttu-id="c29fd-124">В этом примере Носучкомпонент отсутствует в [таблице Component](component-table.md) , а носучфеатуре отсутствует в [таблице Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c29fd-124">In this example, NoSuchComponent is absent from the [Component table](component-table.md) and NoSuchFeature is absent from the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="c29fd-125">[Таблица инсталлексекутесекуенце](installexecutesequence-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="c29fd-125">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="c29fd-126">Действие</span><span class="sxs-lookup"><span data-stu-id="c29fd-126">Action</span></span>  | <span data-ttu-id="c29fd-127">Условие</span><span class="sxs-lookup"><span data-stu-id="c29fd-127">Condition</span></span>                                |
|---------|------------------------------------------|
| <span data-ttu-id="c29fd-128">Custom1</span><span class="sxs-lookup"><span data-stu-id="c29fd-128">Custom1</span></span> | <span data-ttu-id="c29fd-129">ТЕСТАКТИОН = 1046 и &Носучфеатуре>2</span><span class="sxs-lookup"><span data-stu-id="c29fd-129">TESTACTION=1046 AND &NoSuchFeature>2</span></span>  |
| <span data-ttu-id="c29fd-130">Custom2</span><span class="sxs-lookup"><span data-stu-id="c29fd-130">Custom2</span></span> | <span data-ttu-id="c29fd-131">ТЕСТАКТИОН = 146 и $NoSuchComponent>2</span><span class="sxs-lookup"><span data-stu-id="c29fd-131">TESTACTION=146 AND $NoSuchComponent>2</span></span> |



 

<span data-ttu-id="c29fd-132">Чтобы устранить эти ошибки, введите допустимые записи для Носучфеатуре и Носучкомпонент в таблицах компонентов и компонентов.</span><span class="sxs-lookup"><span data-stu-id="c29fd-132">To fix these errors, enter valid records for NoSuchFeature and NoSuchComponent in the Feature and Component tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c29fd-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c29fd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c29fd-134">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c29fd-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



