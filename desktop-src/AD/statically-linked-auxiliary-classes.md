---
title: Статически связанные вспомогательные классы
description: Статически связываемый вспомогательный класс — это тот, который включен в атрибут auxiliaryClass или Системауксилиарикласс определения classSchema класса объекта в схеме.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Статически связанные вспомогательные классы AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773073"
---
# <a name="statically-linked-auxiliary-classes"></a><span data-ttu-id="d6d4b-104">Статически связанные вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="d6d4b-104">Statically Linked Auxiliary Classes</span></span>

<span data-ttu-id="d6d4b-105">Статически связываемый вспомогательный класс — это тот, который включен в атрибут **auxiliaryClass** или **системауксилиарикласс** определения **classSchema** класса объекта в схеме.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-105">A statically linked auxiliary class is one that is included in the **auxiliaryClass** or **systemAuxiliaryClass** attribute of an object class's **classSchema** definition in the schema.</span></span> <span data-ttu-id="d6d4b-106">Это означает, что вспомогательный класс является частью каждого экземпляра класса, с которым он связан.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-106">This means that the auxiliary class is part of every instance of the class with which it is associated.</span></span>

<span data-ttu-id="d6d4b-107">Вспомогательный класс может быть статически связан с классом объекта, если определен класс, то есть когда его объект **classSchema** добавляется в контейнер схемы.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-107">An auxiliary class can be statically linked to an object class when the class is defined, that is, when its **classSchema** object is added to the schema container.</span></span> <span data-ttu-id="d6d4b-108">Это единственный момент, когда можно использовать **системауксилиарикласс** . После создания объекта **classSchema** его атрибут **системауксилиарикласс** нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-108">This is the only time that the **systemAuxiliaryClass** can be used; after a **classSchema** object is created, its **systemAuxiliaryClass** attribute cannot be modified.</span></span> <span data-ttu-id="d6d4b-109">Вспомогательный класс, который статически связывается в это время, может иметь обязательные (**муссаве**) и (или) необязательные (**майхаве**) атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-109">An auxiliary class that is statically linked at this time can have mandatory (**mustHave**) and/or optional (**mayHave**) attributes.</span></span>

<span data-ttu-id="d6d4b-110">Привилегированный пользователь с разрешениями, необходимыми для расширения схемы, может добавлять или удалять вспомогательные классы из атрибута **системауксилиарикласс** существующего объекта **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="d6d4b-110">A privileged user with the permissions required to extend the schema can add or remove auxiliary classes from the **systemAuxiliaryClass** attribute of an existing **classSchema** object.</span></span> <span data-ttu-id="d6d4b-111">Это приводит к добавлению или удалению вспомогательного класса из каждого существующего экземпляра класса Object.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-111">Doing so adds or removes the auxiliary class from every existing instance of the object class.</span></span> <span data-ttu-id="d6d4b-112">Вспомогательный класс, который статически связывается в этот момент, может иметь необязательные атрибуты, но не может иметь обязательные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-112">An auxiliary class that is statically linked at this time can have optional attributes, but cannot have mandatory attributes.</span></span> <span data-ttu-id="d6d4b-113">Это связано с тем, что могут существовать существующие экземпляры класса Object. в этом случае Добавление нового обязательного атрибута может привести к проблемам.</span><span class="sxs-lookup"><span data-stu-id="d6d4b-113">This is because there may be existing instances of the object class, in which case, adding a new mandatory attribute would create problems.</span></span> <span data-ttu-id="d6d4b-114">Привилегированный пользователь может впоследствии удалить вспомогательный класс из атрибута **auxiliaryClass** объекта **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="d6d4b-114">A privileged user can subsequently remove an auxiliary class from the **auxiliaryClass** attribute of a **classSchema** object.</span></span>

 

 




