---
title: Интеграция расширений схемы с пользовательским интерфейсом
description: Средства администрирования служб домен Active Directory Services используют общую архитектуру для подключения пользовательского интерфейса администратора к схеме каталога.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654179"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a><span data-ttu-id="0f690-103">Интеграция расширений схемы с пользовательским интерфейсом</span><span class="sxs-lookup"><span data-stu-id="0f690-103">Integrating Schema Extensions with the User Interface</span></span>

<span data-ttu-id="0f690-104">Средства администрирования служб домен Active Directory Services используют общую архитектуру для подключения пользовательского интерфейса администратора к схеме каталога.</span><span class="sxs-lookup"><span data-stu-id="0f690-104">The administration tools of Active Directory Domain Services use a common architecture for connecting the administrative user interface to the directory schema.</span></span> <span data-ttu-id="0f690-105">Стать центральным элементом этой архитектуры является класс объекта **дисплайспеЦифиер** .</span><span class="sxs-lookup"><span data-stu-id="0f690-105">The centerpiece of this architecture is the **displaySpecifier** object class.</span></span> <span data-ttu-id="0f690-106">Описатели отображения и их использование подробно описаны в разделе [расширение пользовательского интерфейса для объектов каталога](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0f690-106">Display specifiers and their usage are described in detail in [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

<span data-ttu-id="0f690-107">При создании нового класса с помощью подкласса существующего класса можно использовать существующий пользовательский интерфейс для суперкласса, скопировав спецификатор экрана суперкласса.</span><span class="sxs-lookup"><span data-stu-id="0f690-107">When you create a new class by subclassing an existing class, you can leverage the existing UI for the superclass by copying the superclass' display specifier.</span></span> <span data-ttu-id="0f690-108">Простой способ скопировать описатель экрана для класса — это экспортировать его в LDIF-файл с помощью LDIFDE, изменить различающееся имя и CN, а затем импортировать измененный LDIF-файл.</span><span class="sxs-lookup"><span data-stu-id="0f690-108">An easy way to copy the display specifier for a class is to export it into an LDIF file using LDIFDE, edit the Distinguished name and CN, then import the modified LDIF file.</span></span> <span data-ttu-id="0f690-109">Если подкласс имеет дополнительные атрибуты, необходимо предоставить дополнительные страницы свойств для поддержки редактирования.</span><span class="sxs-lookup"><span data-stu-id="0f690-109">If the subclass has additional attributes, you will need to provide additional property pages to support editing.</span></span> <span data-ttu-id="0f690-110">Если подкласс имеет дополнительные свойства, необходимо предоставить страницы расширения диалогового окна создания, так как пользовательский интерфейс, предоставленный суперклассом, не имеет возможности создавать эти новые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0f690-110">If the subclass has additional must-have properties, you will need to provide Creation Dialog extension pages since the UI provided by the superclass has no way to create these new attributes.</span></span>

 

 




