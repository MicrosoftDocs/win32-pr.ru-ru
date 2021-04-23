---
description: Системы на базе Windows могут иметь несколько экземпляров типа объекта Трустеддомаин.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Тип объекта Трустеддомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809293"
---
# <a name="the-trusteddomain-object-type"></a><span data-ttu-id="d9992-103">Тип объекта Трустеддомаин</span><span class="sxs-lookup"><span data-stu-id="d9992-103">The TrustedDomain Object Type</span></span>

<span data-ttu-id="d9992-104">Системы на базе Windows могут иметь несколько экземпляров типа объекта [**трустеддомаин**](trusteddomain-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d9992-104">Windows-based systems can have multiple instances of the [**TrustedDomain**](trusteddomain-object.md) object type.</span></span> <span data-ttu-id="d9992-105">Объекты **трустеддомаин** имеют два поля, которые должны быть уникальными для всех объектов **трустеддомаин** :</span><span class="sxs-lookup"><span data-stu-id="d9992-105">**TrustedDomain** objects have two fields that must be unique among all **TrustedDomain** objects:</span></span>

-   <span data-ttu-id="d9992-106">Имя [ **трустеддомаин**](trusteddomain-object.md)</span><span class="sxs-lookup"><span data-stu-id="d9992-106">The name of the [**TrustedDomain**](trusteddomain-object.md)</span></span>
-   <span data-ttu-id="d9992-107">[*Идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID) [**трустеддомаин**](trusteddomain-object.md).</span><span class="sxs-lookup"><span data-stu-id="d9992-107">The [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the [**TrustedDomain**](trusteddomain-object.md).</span></span>

<span data-ttu-id="d9992-108">Попытка создать новый объект **трустеддомаин** с именем или идентификатором безопасности, который уже используется другим объектом **трустеддомаин** , будет отклонен.</span><span class="sxs-lookup"><span data-stu-id="d9992-108">An attempt to create a new **TrustedDomain** object with either a name or SID that is already in use by another **TrustedDomain** object will be rejected.</span></span>

 

 
