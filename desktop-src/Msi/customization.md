---
description: Поскольку установщик Windows сохраняет все сведения об установке в реляционной базе данных, установку приложения или продукта можно настроить для определенных групп пользователей, применяя операции преобразования к пакету.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662493"
---
# <a name="customization"></a><span data-ttu-id="0f035-103">Настройка</span><span class="sxs-lookup"><span data-stu-id="0f035-103">Customization</span></span>

<span data-ttu-id="0f035-104">Поскольку установщик Windows сохраняет все сведения об установке в реляционной базе данных, установку приложения или продукта можно настроить для определенных групп пользователей, применяя операции преобразования к пакету.</span><span class="sxs-lookup"><span data-stu-id="0f035-104">Because the Windows Installer keeps all information about the installation in a relational database, the installation of an application or product can be customized for particular user groups by applying transform operations to the package.</span></span> <span data-ttu-id="0f035-105">Преобразования можно использовать для инкапсуляции различных настроек основного пакета, которые требуются для различных рабочих групп.</span><span class="sxs-lookup"><span data-stu-id="0f035-105">Transforms can be used to encapsulate the various customizations of a base package required by different workgroups.</span></span> <span data-ttu-id="0f035-106">Дополнительные сведения см. в разделе [слияния и преобразования](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="0f035-106">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

<span data-ttu-id="0f035-107">Во время установки несколько преобразований базового пакета могут быть применены в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="0f035-107">Multiple transforms of a base package can be applied on-the-fly during installation.</span></span> <span data-ttu-id="0f035-108">Это обеспечивает механизм эффективного назначения настраиваемых установок разным группам пользователей.</span><span class="sxs-lookup"><span data-stu-id="0f035-108">This provides a mechanism for efficiently assigning customized installations to different groups of users.</span></span> <span data-ttu-id="0f035-109">Например, это может быть полезно в организациях, где отделы поддержки финансов и штатного отдела требуют различных установок конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="0f035-109">For example, this would be useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="0f035-110">Продукт можно сделать доступным для всех пользователей в Организации с помощью [административной установки](administrative-installation.md) базового пакета в одну точку административной установки.</span><span class="sxs-lookup"><span data-stu-id="0f035-110">The product can be made available to everyone in the organization by an [administrative installation](administrative-installation.md) of the base package to a single administrative installation point.</span></span> <span data-ttu-id="0f035-111">Каждая Рабочая группа может автоматически получить соответствующую настройку с помощью преобразования "на лету" при установке продукта.</span><span class="sxs-lookup"><span data-stu-id="0f035-111">Each work group can then automatically receive their appropriate customization by means of an on-the-fly transform when they install the product.</span></span>

 

 



