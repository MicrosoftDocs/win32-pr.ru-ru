---
title: Компонент примера поставщика ADSI
description: Модули записи поставщика интерфейсов служб Active Directory найдут этот раздел определенного интереса, так как в нем подробно описывается компонент поставщика в примере ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328451"
---
# <a name="adsi-example-provider-component"></a><span data-ttu-id="73418-103">Компонент примера поставщика ADSI</span><span class="sxs-lookup"><span data-stu-id="73418-103">ADSI Example Provider Component</span></span>

<span data-ttu-id="73418-104">Модули записи поставщика интерфейсов служб Active Directory найдут этот раздел определенного интереса, так как в нем подробно описывается компонент поставщика в примере ADSI.</span><span class="sxs-lookup"><span data-stu-id="73418-104">Active Directory Service Interfaces provider writers will find this section of particular interest, because it describes the ADSI example provider component in depth.</span></span> <span data-ttu-id="73418-105">Модули записи поставщика ADSI могут установить пример поставщика и использовать платформу кода как основу для создания собственной реализации.</span><span class="sxs-lookup"><span data-stu-id="73418-105">ADSI provider writers can install the example provider and use the code framework as a basis to create their own implementation.</span></span> <span data-ttu-id="73418-106">Рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="73418-106">The following topics are discussed:</span></span>

<span data-ttu-id="73418-107">[Установка компонента "пример поставщика"](installing-the-example-provider-component.md) описывается в статье Установка поставщика ADSI и каталога макета.</span><span class="sxs-lookup"><span data-stu-id="73418-107">[Installing the Example Provider Component](installing-the-example-provider-component.md) describes how to install the ADSI sample provider and its mock directory.</span></span> <span data-ttu-id="73418-108">Этот раздел содержит список параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="73418-108">This section includes a list of the registry settings.</span></span>

<span data-ttu-id="73418-109">[Определение каталога](directory-definition.md) описывает записи каталога, определенные в примере компонента поставщика.</span><span class="sxs-lookup"><span data-stu-id="73418-109">[Directory Definition](directory-definition.md) describes the directory entries defined by the example provider component.</span></span>

<span data-ttu-id="73418-110">[Управление схемой](schema-management.md) описывает, как каждый элемент в примере службы каталогов компонента поставщика может быть представлен конкретным типом объекта Active Directory.</span><span class="sxs-lookup"><span data-stu-id="73418-110">[Schema Management](schema-management.md) describes how each element in the example provider component directory service can be represented by a specific type of Active Directory object.</span></span>

<span data-ttu-id="73418-111">[Привязка к объекту Active Directory](binding-to-an-active-directory-object.md) описывает, как, учитывая строку ADsPath, компонент поставщика примера определяет этот элемент, создает для него соответствующий тип объекта Active Directory и извлекает запрошенный тип указателя интерфейса на этот объект для передачи в клиентское программное обеспечение ADS.</span><span class="sxs-lookup"><span data-stu-id="73418-111">[Binding to an Active Directory Object](binding-to-an-active-directory-object.md) describes how, given an ADsPath string, the example provider component identifies that element, creates the appropriate type of Active Directory object for it, and retrieves the requested type of interface pointer on that object to pass back to the ADs client software.</span></span>

<span data-ttu-id="73418-112">[Объекты перечислителя](enumerator-objects.md) перечисляет конкретные типы перечислений, предоставляемые компонентом "пример поставщика", а также исходный код, в котором можно найти реализации.</span><span class="sxs-lookup"><span data-stu-id="73418-112">[Enumerator Objects](enumerator-objects.md) lists the specific types of enumerations supplied by the example provider component and in which source code the implementations can be found.</span></span>

<span data-ttu-id="73418-113">[Общие сведения о коде](code-overview.md) предоставляют описание уровня задачи для каждой части компонента примера поставщика.</span><span class="sxs-lookup"><span data-stu-id="73418-113">[Code Overview](code-overview.md) provides a task-level description of each part of the example provider component.</span></span>

<span data-ttu-id="73418-114">В [сведениях о коде](code-details.md) перечислены программные модули и их содержимое.</span><span class="sxs-lookup"><span data-stu-id="73418-114">[Code Details](code-details.md) lists the software modules and their contents.</span></span>

 

 




