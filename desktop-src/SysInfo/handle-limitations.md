---
description: Некоторые объекты поддерживают только один обработчик за раз.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Ограничения по обработке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272247"
---
# <a name="handle-limitations"></a><span data-ttu-id="3aa29-103">Ограничения по обработке</span><span class="sxs-lookup"><span data-stu-id="3aa29-103">Handle Limitations</span></span>

<span data-ttu-id="3aa29-104">Некоторые объекты поддерживают только один обработчик за раз.</span><span class="sxs-lookup"><span data-stu-id="3aa29-104">Some objects support only one handle at a time.</span></span> <span data-ttu-id="3aa29-105">Система предоставляет обработчик, когда приложение создает объект и делает его недействительным, когда приложение уничтожает объект.</span><span class="sxs-lookup"><span data-stu-id="3aa29-105">The system provides the handle when an application creates the object and invalidates the handle when the application destroys the object.</span></span> <span data-ttu-id="3aa29-106">Другие объекты поддерживают несколько дескрипторов для одного объекта.</span><span class="sxs-lookup"><span data-stu-id="3aa29-106">Other objects support multiple handles to a single object.</span></span> <span data-ttu-id="3aa29-107">Операционная система автоматически удаляет объект из памяти после закрытия последнего маркера объекта.</span><span class="sxs-lookup"><span data-stu-id="3aa29-107">The operating system automatically removes the object from memory after the last handle to the object is closed.</span></span>

<span data-ttu-id="3aa29-108">Общее число открытых дескрипторов в системе ограничено только объемом доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="3aa29-108">The total number of open handles in the system is limited only by the amount of memory available.</span></span> <span data-ttu-id="3aa29-109">Некоторые типы объектов поддерживают ограниченное количество дескрипторов для одного сеанса или для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="3aa29-109">Some object types support a limited number of handles per session or per process.</span></span>

 

 



