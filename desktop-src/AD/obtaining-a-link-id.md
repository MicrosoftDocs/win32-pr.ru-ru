---
title: Получение идентификатора ссылки
description: Начиная с Windows Server 2003, больше не требуется запрашивать linkID в корпорации Майкрософт; Существует процесс автоматического создания linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Получение идентификатора ссылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133674"
---
# <a name="obtaining-a-link-id"></a><span data-ttu-id="8dbc0-104">Получение идентификатора ссылки</span><span class="sxs-lookup"><span data-stu-id="8dbc0-104">Obtaining a Link ID</span></span>

<span data-ttu-id="8dbc0-105">Начиная с Windows Server 2003, больше не требуется запрашивать [**LinkId**](/windows/desktop/ADSchema/a-linkid) в корпорации Майкрософт; Существует процесс автоматического создания **LinkId**.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-105">Starting with Windows Server 2003, it is no longer necessary to request a [**linkID**](/windows/desktop/ADSchema/a-linkid) from Microsoft; there is a process for automatically generating a **linkID**.</span></span> <span data-ttu-id="8dbc0-106">Система автоматически создаст идентификатор ссылки для нового связанного атрибута, если атрибут **LinkId** атрибута имеет значение 1.2.840.113556.1.2.50.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-106">The system will automatically generate a link ID for a new linked attribute when the attribute's **linkID** attribute is set to 1.2.840.113556.1.2.50.</span></span> <span data-ttu-id="8dbc0-107">Чтобы создать ссылку назад для этой прямой ссылки, необходимо задать для параметра **LinkId** значение [**attributeID**](/windows/desktop/ADSchema/a-attributeid) или [**LdapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) для прямой ссылки.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-107">A back link for this forward link is created by setting the **linkID** to the [**attributeID**](/windows/desktop/ADSchema/a-attributeid) or [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) of the forward link.</span></span> <span data-ttu-id="8dbc0-108">Кэш схемы должен быть перезагружен после создания ссылки вперед и перед созданием ссылки назад.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-108">The schema cache must be reloaded after creating the forward link and before creating the back link.</span></span> <span data-ttu-id="8dbc0-109">В противном случае обратная ссылка **attributeID** или **LdapDisplayName** не будет найдена при создании ссылки на нее.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-109">Otherwise, the forward link's **attributeId** or **ldapDisplayName** will not be found when the back link is created.</span></span> <span data-ttu-id="8dbc0-110">Кэш схемы перезагружается по запросу, через несколько минут после внесения изменений схемы или после перезапуска контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-110">The schema cache is reloaded on demand, a few minutes after a schema change is made, or when the DC is restarted.</span></span> <span data-ttu-id="8dbc0-111">Создайте все прямые ссылки, перезагрузите кэш схемы, а затем создайте все обратные ссылки.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-111">Create all forward links, reload the schema cache and then create all back links.</span></span>

<span data-ttu-id="8dbc0-112">Например, если вы создали новые атрибуты **мифорвардлинкаттр** и **мибакклинкаттр** и хотите связать их:</span><span class="sxs-lookup"><span data-stu-id="8dbc0-112">For example, when you have created the new attributes **myForwardLinkAttr** and **myBackLinkAttr**, and wish to link them:</span></span>

> [!Note]  
> <span data-ttu-id="8dbc0-113">OID в этом примере — надуманный.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-113">The OIDs in this example are contrived.</span></span> <span data-ttu-id="8dbc0-114">Инструкции по получению идентификаторов объектов (OID) для новых атрибутов см. в разделе [Получение идентификатора объекта от корпорации Майкрософт](obtaining-an-object-identifier-from-microsoft.md) .</span><span class="sxs-lookup"><span data-stu-id="8dbc0-114">See [Obtaining an Object Identifier from Microsoft](obtaining-an-object-identifier-from-microsoft.md) for instructions on obtaining OIDs for new attributes.</span></span>

 

1.  <span data-ttu-id="8dbc0-115">Задайте эти атрибуты для атрибута, который должен быть прямой ссылкой:</span><span class="sxs-lookup"><span data-stu-id="8dbc0-115">Set these attributes on the attribute that is to be the forward link:</span></span>
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  <span data-ttu-id="8dbc0-116">Перезагрузите схему.</span><span class="sxs-lookup"><span data-stu-id="8dbc0-116">Reload the Schema.</span></span>
3.  <span data-ttu-id="8dbc0-117">Задайте эти атрибуты для атрибута, который должен быть обратной связью:</span><span class="sxs-lookup"><span data-stu-id="8dbc0-117">Set these attributes on the attribute that is to be the back link:</span></span>
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a><span data-ttu-id="8dbc0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="8dbc0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dbc0-119">Связанные атрибуты</span><span class="sxs-lookup"><span data-stu-id="8dbc0-119">Linked Attributes</span></span>](linked-attributes.md)
</dt> <dt>

[<span data-ttu-id="8dbc0-120">Расширение схемы</span><span class="sxs-lookup"><span data-stu-id="8dbc0-120">How to Extend the Schema</span></span>](how-to-extend-the-schema.md)
</dt> </dl>

 

 