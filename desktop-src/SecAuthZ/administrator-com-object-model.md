---
description: Приложение, выполняющееся в качестве обычного пользователя, выполняет операции, требующие прав администратора, создавая объект модели объектов с повышенными правами.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Модель COM-объектов администратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911843"
---
# <a name="administrator-com-object-model"></a><span data-ttu-id="e3f9c-103">Модель COM-объектов администратора</span><span class="sxs-lookup"><span data-stu-id="e3f9c-103">Administrator COM Object Model</span></span>

<span data-ttu-id="e3f9c-104">В модели COM-объекта администратора приложение, выполняемое в качестве обычного пользователя, выполняет операции, требующие прав администратора, создавая объект [модели объектов](/windows/desktop/com/component-object-model--com--portal) с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="e3f9c-104">In the administrator COM object model, an application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> <span data-ttu-id="e3f9c-105">Сведения о создании COM-объекта с повышенными привилегиями см. в описании [моникера повышения уровня com](../com/the-com-elevation-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="e3f9c-105">For information about creating an elevated COM object, see [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).</span></span>

<span data-ttu-id="e3f9c-106">Недостаток использования объектной модели COM администратора заключается в том, что пользователю предлагается каждый раз при выполнении привилегированной операции.</span><span class="sxs-lookup"><span data-stu-id="e3f9c-106">One drawback to using the administrator COM object model is that the user is prompted each time a privileged operation is performed.</span></span>

<span data-ttu-id="e3f9c-107">Любой пользовательский интерфейс, который может управлять COM-объектом, должен быть представлен самим COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="e3f9c-107">Any user interface that can control the COM object must be presented by the COM object itself.</span></span> <span data-ttu-id="e3f9c-108">В противном случае непривилегированный процесс может привести к тому, что COM-объект с повышенными правами сможет выполнять привилегированные операции без запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="e3f9c-108">Otherwise, an unprivileged process could cause the elevated COM object to perform privileged operations without the user being prompted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3f9c-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e3f9c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3f9c-110">Разработка приложений, требующих прав администратора</span><span class="sxs-lookup"><span data-stu-id="e3f9c-110">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="e3f9c-111">Модель брокера администратора</span><span class="sxs-lookup"><span data-stu-id="e3f9c-111">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="e3f9c-112">Модель задач с повышенными правами</span><span class="sxs-lookup"><span data-stu-id="e3f9c-112">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> <dt>

[<span data-ttu-id="e3f9c-113">Модель службы операционной системы</span><span class="sxs-lookup"><span data-stu-id="e3f9c-113">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
