---
title: Внедренные объекты (COM)
description: Внедренные объекты
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134926"
---
# <a name="embedded-objects-com"></a><span data-ttu-id="d2b77-103">Внедренные объекты (COM)</span><span class="sxs-lookup"><span data-stu-id="d2b77-103">Embedded Objects (COM)</span></span>

<span data-ttu-id="d2b77-104">Внедренный объект физически хранится в составном документе вместе со всеми сведениями, необходимыми для управления объектом.</span><span class="sxs-lookup"><span data-stu-id="d2b77-104">An embedded object is physically stored in the compound document, along with all the information needed to manage the object.</span></span> <span data-ttu-id="d2b77-105">Другими словами, внедренный объект на самом деле является частью составного документа, в котором он находится.</span><span class="sxs-lookup"><span data-stu-id="d2b77-105">In other words, the embedded object is actually a part of the compound document in which it resides.</span></span> <span data-ttu-id="d2b77-106">Это расположение имеет несколько недостатков.</span><span class="sxs-lookup"><span data-stu-id="d2b77-106">This arrangement has a couple of disadvantages.</span></span> <span data-ttu-id="d2b77-107">Во-первых, составной документ, содержащий внедренные объекты, будет больше, чем один, содержащий те же объекты, что и ссылки.</span><span class="sxs-lookup"><span data-stu-id="d2b77-107">First, a compound document containing embedded objects will be larger than one containing the same objects as links.</span></span> <span data-ttu-id="d2b77-108">Во-вторых, изменения, вносимые в источник внедренного объекта, не будут автоматически реплицироваться во внедренную копию, а изменения в внедренной копии не будут отражены в источнике, так как они связаны с ссылкой.</span><span class="sxs-lookup"><span data-stu-id="d2b77-108">Second, changes made to the source of an embedded object will not be automatically replicated in the embedded copy, and changes in the embedded copy will not be reflected in the source, as they are with a link.</span></span>

<span data-ttu-id="d2b77-109">По-прежнему для определенных целей внедрение предлагает несколько преимуществ по сравнению с ссылками.</span><span class="sxs-lookup"><span data-stu-id="d2b77-109">Still, for certain purposes, embedding offers several advantages over links.</span></span> <span data-ttu-id="d2b77-110">Во-первых, пользователи могут передавать составные документы с внедренными объектами на другие компьютеры или другие расположения на том же компьютере без разрыва связи.</span><span class="sxs-lookup"><span data-stu-id="d2b77-110">First, users can transfer compound documents with embedded objects to other computers, or other locations on the same computer, without breaking a link.</span></span> <span data-ttu-id="d2b77-111">Во вторых, пользователи могут изменять внедренные объекты, не изменяя содержимое исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2b77-111">Second, users can edit embedded objects without changing the content of the original.</span></span> <span data-ttu-id="d2b77-112">Иногда это разделение является именно необходимым.</span><span class="sxs-lookup"><span data-stu-id="d2b77-112">Sometimes, this separation is precisely what is required.</span></span> <span data-ttu-id="d2b77-113">В-третьих, внедренные объекты могут быть активированы на месте, что означает, что пользователь может редактировать объект или иным образом манипулировать им, не прибегая к работе в отдельном окне из контейнера объекта.</span><span class="sxs-lookup"><span data-stu-id="d2b77-113">Third, embedded objects can be activated in place, meaning that the user can edit or otherwise manipulate the object without having to work in a separate window from that of the object's container.</span></span> <span data-ttu-id="d2b77-114">Вместо этого при активации объекта пользовательский интерфейс приложения контейнера изменяется для предоставления средств, необходимых для управления или изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="d2b77-114">Instead, when the object is activated, the container application's user interface changes to expose those tools that are necessary to manage or modify the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2b77-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d2b77-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2b77-116">Создание связанных и внедренных объектов из существующих данных</span><span class="sxs-lookup"><span data-stu-id="d2b77-116">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




