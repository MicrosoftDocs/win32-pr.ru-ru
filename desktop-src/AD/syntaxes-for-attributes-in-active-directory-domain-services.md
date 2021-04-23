---
title: Синтаксис атрибутов в домен Active Directory Services
description: Домен Active Directory Services определяют набор синтаксисов атрибутов для указания типа данных, содержащихся в атрибуте.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Синтаксис для атрибутов домен Active Directory Services Active Directory
- Атрибуты Active Directory, синтаксис для
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133647"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a><span data-ttu-id="de748-105">Синтаксис атрибутов в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="de748-105">Syntaxes for Attributes in Active Directory Domain Services</span></span>

<span data-ttu-id="de748-106">Домен Active Directory Services определяют набор синтаксисов атрибутов для указания типа данных, содержащихся в атрибуте.</span><span class="sxs-lookup"><span data-stu-id="de748-106">Active Directory Domain Services define a set of attribute syntaxes for specifying the type of data contained by an attribute.</span></span> <span data-ttu-id="de748-107">Предопределенные синтаксисы фактически не отображаются в каталоге и не могут добавлять новые синтаксисы.</span><span class="sxs-lookup"><span data-stu-id="de748-107">The predefined syntaxes do not actually appear in the directory, and you cannot add new syntaxes.</span></span> <span data-ttu-id="de748-108">Для обнаружения синтаксиса класса атрибута можно использовать несколько методов:</span><span class="sxs-lookup"><span data-stu-id="de748-108">Several methods can be used to identify the syntax of an attribute class:</span></span>

-   <span data-ttu-id="de748-109">Методы [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**iAds. жетекс**](/windows/desktop/api/iads/nf-iads-iads-getex), [**iAds.**](/windows/desktop/api/iads/nf-iads-iads-put)WHERE и [**iAds. путекс**](/windows/desktop/api/iads/nf-iads-iads-putex) используют структуру [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) для получения и задания значений атрибутов объекта.</span><span class="sxs-lookup"><span data-stu-id="de748-109">The [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs.GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put), and [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) methods use the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure to get and set the values of an object's attributes.</span></span> <span data-ttu-id="de748-110">Элемент **VT** этой структуры является значением **VarType** , определяющим тип данных.</span><span class="sxs-lookup"><span data-stu-id="de748-110">The **vt** member of this structure is a **VARTYPE** value that identifies the data type.</span></span>
-   <span data-ttu-id="de748-111">Методы интерфейсов [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) и [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) используют значение из перечисления [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) для указания типа данных.</span><span class="sxs-lookup"><span data-stu-id="de748-111">The methods of the [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interfaces use a value from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration to specify the data type.</span></span>
-   <span data-ttu-id="de748-112">Чтобы указать синтаксис нового класса атрибута, установите атрибуты [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) и [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) .</span><span class="sxs-lookup"><span data-stu-id="de748-112">To specify the syntax of a new attribute class, set the [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) and [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) attributes of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object.</span></span> <span data-ttu-id="de748-113">Если значение **oMSyntax** равно 127, необходимо также задать атрибут [**омобжекткласс**](/windows/desktop/ADSchema/a-omobjectclass) .</span><span class="sxs-lookup"><span data-stu-id="de748-113">If the value of **oMSyntax** is 127, you must also set the [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) attribute.</span></span> <span data-ttu-id="de748-114">Дополнительные сведения см. [в разделе Выбор синтаксиса](choosing-a-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="de748-114">For more information, see [Choosing a Syntax](choosing-a-syntax.md).</span></span>

<span data-ttu-id="de748-115">Полный список синтаксиса, предоставляемого домен Active Directory Services, включая соответствующие значения **VarType** и [**адстипинум**](/windows/win32/api/iads/ne-iads-adstypeenum) для каждого синтаксиса, см. в разделе [синтаксисы](/windows/desktop/ADSchema/syntaxes).</span><span class="sxs-lookup"><span data-stu-id="de748-115">For a complete list of the syntaxes provided by Active Directory Domain Services, including each syntax's corresponding **VARTYPE** and [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value, see [Syntaxes](/windows/desktop/ADSchema/syntaxes).</span></span>

 

 