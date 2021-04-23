---
description: Родительские элементы управления и контроль учетных записей пользователей
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Родительские элементы управления и контроль учетных записей пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711945"
---
# <a name="parental-controls-and-user-account-control"></a><span data-ttu-id="262c2-103">Родительские элементы управления и контроль учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="262c2-103">Parental Controls and User Account Control</span></span>

<span data-ttu-id="262c2-104">Управление учетными записями пользователей (UAC) приведет к наличию учетных записей защищенного администратора и обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="262c2-104">User Account Control (UAC) will result in presence of Protected Administrator and Standard User accounts.</span></span> <span data-ttu-id="262c2-105">Защищенный администратор будет работать с теми же правами, что и Стандартный пользователь при нормальном использовании.</span><span class="sxs-lookup"><span data-stu-id="262c2-105">A Protected Administrator will run with the same rights as a Standard User under normal usage.</span></span> <span data-ttu-id="262c2-106">Для привилегированных операций:</span><span class="sxs-lookup"><span data-stu-id="262c2-106">For privileged operations:</span></span>

-   <span data-ttu-id="262c2-107">Стандартный пользователь будет отображаться в диалоговом окне Пользовательский интерфейс учетных данных, в котором необходимо ввести имя пользователя и пароль для защищенного администратора или встроенного администратора.</span><span class="sxs-lookup"><span data-stu-id="262c2-107">A Standard User will be shown the Credentials User Interface dialog box, which requires the input of a user name and password for a Protected Administrator or built-in Administrator.</span></span>
-   <span data-ttu-id="262c2-108">Защищенный администратор будет отображен в диалоговом окне Пользовательский интерфейс согласия, для которого необходимо выбрать разрешить продолжение.</span><span class="sxs-lookup"><span data-stu-id="262c2-108">A Protected Administrator will be shown the Consent User Interface dialog box, which requires selection of Allow to proceed.</span></span>

<span data-ttu-id="262c2-109">Важно отметить, что UAC реализуется отдельно для каждого процесса, поэтому процесс либо выполняется с повышенными правами, либо нет.</span><span class="sxs-lookup"><span data-stu-id="262c2-109">It is important to note that UAC is implemented on a per-process basis, so a process either runs elevated or not.</span></span> <span data-ttu-id="262c2-110">Как правило, он не подходит для запуска больших приложений с точки зрения безопасности, так как всегда имеет повышенный уровень прав.</span><span class="sxs-lookup"><span data-stu-id="262c2-110">Generally, it is not suitable from a security standpoint to run large applications as always elevated.</span></span> <span data-ttu-id="262c2-111">Для родительских элементов управления код, который должен изменить параметры, должен быть изолирован одним из двух вариантов реализации:</span><span class="sxs-lookup"><span data-stu-id="262c2-111">For Parental Controls, code that must modify settings should be isolated by one of two implementation options:</span></span>

1.  <span data-ttu-id="262c2-112">Создайте небольшой исполняемый файл для управления параметрами, помеченный в его манифесте как обязательные права администратора.</span><span class="sxs-lookup"><span data-stu-id="262c2-112">Create a small executable for settings management that is marked in its manifest as requiring administrative rights.</span></span> <span data-ttu-id="262c2-113">Вызов исполняемого файла приведет к отображению пользовательского интерфейса согласия или учетных данных перед тем, как разрешить выполнение процесса.</span><span class="sxs-lookup"><span data-stu-id="262c2-113">Invocation of the executable will cause the Consent or Credentials UI to be shown prior to allowing the process to run.</span></span>
2.  <span data-ttu-id="262c2-114">Предоставьте COM-интерфейсы в библиотеке DLL продукта, которая разрешает вызов для каждой документации по UAC.</span><span class="sxs-lookup"><span data-stu-id="262c2-114">Provide COM interfaces in a product DLL that allow for invocation per UAC documentation.</span></span> <span data-ttu-id="262c2-115">Это также приведет к отображению соответствующего пользовательского интерфейса согласия или учетных данных.</span><span class="sxs-lookup"><span data-stu-id="262c2-115">This will also cause the appropriate Consent or Credentials UI to be shown.</span></span>

 

 



