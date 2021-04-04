---
description: ICE58 проверяет, что в таблице мультимедиа не более 80 строк.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999107"
---
# <a name="ice58"></a><span data-ttu-id="c460a-103">ICE58</span><span class="sxs-lookup"><span data-stu-id="c460a-103">ICE58</span></span>

<span data-ttu-id="c460a-104">ICE58 проверяет, что в [таблице мультимедиа](media-table.md) не более 80 строк.</span><span class="sxs-lookup"><span data-stu-id="c460a-104">ICE58 checks that your [Media table](media-table.md) does not have more than 80 rows.</span></span>

## <a name="result"></a><span data-ttu-id="c460a-105">Результат</span><span class="sxs-lookup"><span data-stu-id="c460a-105">Result</span></span>

<span data-ttu-id="c460a-106">Предупреждения, о которых сообщает ICE58, приводят к сбою установки, если пакет не установлен с установщик Windows 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c460a-106">Warnings reported by ICE58 cause the installation to fail unless the package is installed with Windows Installer 2.0 or later.</span></span> <span data-ttu-id="c460a-107">Начиная с установщик Windows 2,0, ограничение на более 80 записей таблицы мультимедиа удаляется.</span><span class="sxs-lookup"><span data-stu-id="c460a-107">Beginning with Windows Installer 2.0, the restriction to more than 80 media table entries is removed.</span></span> <span data-ttu-id="c460a-108">Если свойство [**сводки количества страниц**](page-count-summary.md) пакета больше или равно 150, предупреждение не выдается.</span><span class="sxs-lookup"><span data-stu-id="c460a-108">No warning is issued if the package's [**Page Count Summary**](page-count-summary.md) Property is greater than or equal to 150.</span></span> <span data-ttu-id="c460a-109">Пакеты схемы 200 или более поздней версии можно установить только установщик Windows 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c460a-109">Packages of schema 200 or higher can only be installed by Windows Installer 2.0 or later.</span></span>

## <a name="example"></a><span data-ttu-id="c460a-110">Пример</span><span class="sxs-lookup"><span data-stu-id="c460a-110">Example</span></span>

<span data-ttu-id="c460a-111">ICE58 сообщает о следующих ошибках и предупреждениях для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="c460a-111">ICE58 reports the following errors and warnings for the example shown.</span></span>

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

<span data-ttu-id="c460a-112">Чтобы устранить эту ошибку, исключите все неиспользуемые записи таблицы мультимедиа, объедините записи таблицы мультимедиа, которые ссылаются на один и тот же носитель, и переупакуйте приложение, чтобы уменьшить необходимый объем носителей.</span><span class="sxs-lookup"><span data-stu-id="c460a-112">To fix this error, eliminate any unused media table entries, consolidate media table entries that refer to the same media, and repackage your application to reduce the media required.</span></span>

<span data-ttu-id="c460a-113">[Таблица мультимедиа](media-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="c460a-113">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="c460a-114">DiskId</span><span class="sxs-lookup"><span data-stu-id="c460a-114">DiskId</span></span> | <span data-ttu-id="c460a-115">ластсекуенце\_</span><span class="sxs-lookup"><span data-stu-id="c460a-115">LastSequence\_</span></span> |
|--------|----------------|
| <span data-ttu-id="c460a-116">1</span><span class="sxs-lookup"><span data-stu-id="c460a-116">1</span></span>      | <span data-ttu-id="c460a-117">10</span><span class="sxs-lookup"><span data-stu-id="c460a-117">10</span></span>             |
| <span data-ttu-id="c460a-118">2</span><span class="sxs-lookup"><span data-stu-id="c460a-118">2</span></span>      | <span data-ttu-id="c460a-119">20</span><span class="sxs-lookup"><span data-stu-id="c460a-119">20</span></span>             |
| <span data-ttu-id="c460a-120">...</span><span class="sxs-lookup"><span data-stu-id="c460a-120">...</span></span>    | <span data-ttu-id="c460a-121">...</span><span class="sxs-lookup"><span data-stu-id="c460a-121">...</span></span>            |
| <span data-ttu-id="c460a-122">81</span><span class="sxs-lookup"><span data-stu-id="c460a-122">81</span></span>     | <span data-ttu-id="c460a-123">810</span><span class="sxs-lookup"><span data-stu-id="c460a-123">810</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="c460a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c460a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c460a-125">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c460a-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



