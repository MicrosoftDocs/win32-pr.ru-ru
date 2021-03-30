---
title: Сравнение одного и нескольких атрибутов значений
description: Атрибуты, которые могут существовать в каталоге, обычно определяются в схеме для каталога.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- Сравнение одного и нескольких атрибутов значений ADSI
- атрибуты ADSI, сравнение одного и нескольких значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067311"
---
# <a name="single-vs-multiple-value-attributes"></a><span data-ttu-id="7e063-105">Сравнение одного и нескольких атрибутов значений</span><span class="sxs-lookup"><span data-stu-id="7e063-105">Single vs. Multiple Value Attributes</span></span>

<span data-ttu-id="7e063-106">Атрибуты, которые могут существовать в каталоге, обычно определяются в схеме для каталога.</span><span class="sxs-lookup"><span data-stu-id="7e063-106">The attributes that can exist in a directory are typically defined in the schema for the directory.</span></span> <span data-ttu-id="7e063-107">Определение схемы атрибута задает ряд характеристик атрибута, например тип данных и возможность наличия у экземпляра атрибута нескольких значений.</span><span class="sxs-lookup"><span data-stu-id="7e063-107">The schema definition of an attribute specifies a number of characteristics of the attribute, such as the data type and whether an instance of the attribute can have multiple values.</span></span>

<span data-ttu-id="7e063-108">Экземпляр атрибута с одним значением может содержать одно значение.</span><span class="sxs-lookup"><span data-stu-id="7e063-108">An instance of a single-valued attribute can contain a single value.</span></span> <span data-ttu-id="7e063-109">Экземпляр многозначного атрибута может содержать одно значение или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="7e063-109">An instance of a multivalued attribute can contain either a single value or multiple values.</span></span> <span data-ttu-id="7e063-110">Active Directory не создает атрибуты с пустыми значениями — либо атрибут содержит допустимое значение, либо он не существует в объекте.</span><span class="sxs-lookup"><span data-stu-id="7e063-110">Active Directory does not create attributes with empty values—either the attribute contains a valid value or it does not exist on the object.</span></span>

> [!Note]  
> <span data-ttu-id="7e063-111">В Active Directory и большинстве серверов LDAP порядок значений в атрибуте с несколькими значениями не определен.</span><span class="sxs-lookup"><span data-stu-id="7e063-111">In Active Directory and most other LDAP servers, the order of values in a multi-valued attribute is undefined.</span></span> <span data-ttu-id="7e063-112">Кроме того, каждое значение атрибута с несколькими значениями должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="7e063-112">Also, each value of a multi-valued attribute must be unique.</span></span>

 

<span data-ttu-id="7e063-113">ADSI обычно загружает данные схемы, если каталог поддерживает схему, как Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7e063-113">ADSI normally loads schema data if your directory supports a schema, as Active Directory does.</span></span> <span data-ttu-id="7e063-114">Так как ADSI знает синтаксис атрибутов в схеме, указывать тип атрибута при доступе к нему не требуется.</span><span class="sxs-lookup"><span data-stu-id="7e063-114">Because ADSI knows the syntax of attributes in the schema, you are not required to specify the attribute type when accessing it.</span></span> <span data-ttu-id="7e063-115">ADSI маршалирует значения атрибутов в соответствующий тип данных, как определено в схеме.</span><span class="sxs-lookup"><span data-stu-id="7e063-115">ADSI marshals attribute values to the appropriate data type as defined in the schema.</span></span>

<span data-ttu-id="7e063-116">Если каталог не имеет схемы, укажите тип данных при доступе к атрибуту.</span><span class="sxs-lookup"><span data-stu-id="7e063-116">If your directory has no schema, supply the data type when accessing an attribute.</span></span>

> [!Note]  
> <span data-ttu-id="7e063-117">Active Directory, Exchange, Windows NT 4,0 и сервер сайта имеют схему.</span><span class="sxs-lookup"><span data-stu-id="7e063-117">Active Directory, Exchange, Windows NT 4.0, and Site Server all have a schema.</span></span> <span data-ttu-id="7e063-118">Кроме того, Active Directory имеет расширяемую схему.</span><span class="sxs-lookup"><span data-stu-id="7e063-118">In addition, Active Directory has an extensible schema.</span></span>

 

 

 




