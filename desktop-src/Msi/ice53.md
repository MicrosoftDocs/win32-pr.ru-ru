---
description: ICE53 проверяет наличие записей в таблице реестра, которые записывают данные частного установщика или значения политики в системный реестр.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651034"
---
# <a name="ice53"></a><span data-ttu-id="f5449-103">ICE53</span><span class="sxs-lookup"><span data-stu-id="f5449-103">ICE53</span></span>

<span data-ttu-id="f5449-104">ICE53 проверяет наличие записей в таблице реестра, которые записывают данные частного установщика или значения политики в системный реестр.</span><span class="sxs-lookup"><span data-stu-id="f5449-104">ICE53 checks for entries in the Registry table that write private installer information or policy values to the system registry.</span></span>

## <a name="result"></a><span data-ttu-id="f5449-105">Результат</span><span class="sxs-lookup"><span data-stu-id="f5449-105">Result</span></span>

<span data-ttu-id="f5449-106">ICE53 отправляет предупреждение, если в таблице реестра указано, что в реестре записывается внутренняя информация или сведения о политике.</span><span class="sxs-lookup"><span data-stu-id="f5449-106">ICE53 posts a warning if the Registry table specifies writing internal or policy information to the registry.</span></span>

## <a name="example"></a><span data-ttu-id="f5449-107">Пример</span><span class="sxs-lookup"><span data-stu-id="f5449-107">Example</span></span>

<span data-ttu-id="f5449-108">ICE53 отправляет следующее предупреждение для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="f5449-108">ICE53 posts the following warning for the example shown.</span></span>

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

<span data-ttu-id="f5449-109">[Таблица реестра](registry-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="f5449-109">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="f5449-110">Реестр</span><span class="sxs-lookup"><span data-stu-id="f5449-110">Registry</span></span>             | <span data-ttu-id="f5449-111">Root</span><span class="sxs-lookup"><span data-stu-id="f5449-111">Root</span></span>         | <span data-ttu-id="f5449-112">Ключ</span><span class="sxs-lookup"><span data-stu-id="f5449-112">Key</span></span>                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5449-113">Registry1</span><span class="sxs-lookup"><span data-stu-id="f5449-113">Registry1</span></span><br/> | <span data-ttu-id="f5449-114">1</span><span class="sxs-lookup"><span data-stu-id="f5449-114">1</span></span><br/> | <span data-ttu-id="f5449-115">**Программное обеспечение** \\ **Политики** \\ **Microsoft** \\ **Windows** \\ **Установщик** \\ **Дисаблероллбакк**</span><span class="sxs-lookup"><span data-stu-id="f5449-115">**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**DisableRollback**</span></span><br/> |



 

<span data-ttu-id="f5449-116">Строка таблицы реестра "Registry1" записывает в реестр значение системной политики, влияющее на установку всех пакетов.</span><span class="sxs-lookup"><span data-stu-id="f5449-116">Registry table row 'Registry1' writes a system policy value in the registry that affects the installation of all packages.</span></span> <span data-ttu-id="f5449-117">В зависимости от пакета можно отключить откат только для этого пакета, задав свойство [**дисаблероллбакк**](-disablerollback.md) в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="f5449-117">Depending on the package, it may be possible to disable rollback for this package alone by setting the [**DISABLEROLLBACK**](-disablerollback.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="f5449-118">См. раздел [ROLLBACK Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="f5449-118">See [Rollback Installation](rollback-installation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5449-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f5449-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5449-120">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="f5449-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




