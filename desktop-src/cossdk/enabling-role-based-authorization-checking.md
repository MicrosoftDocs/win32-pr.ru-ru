---
description: Чтобы использовать безопасность на основе ролей в приложении COM+, необходимо сначала включить проверку авторизации на основе ролей для приложения.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Включение проверки авторизации Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072486"
---
# <a name="enabling-role-based-authorization-checking"></a><span data-ttu-id="8a154-103">Включение проверки авторизации Role-Based</span><span class="sxs-lookup"><span data-stu-id="8a154-103">Enabling Role-Based Authorization Checking</span></span>

<span data-ttu-id="8a154-104">Чтобы использовать безопасность на основе ролей в приложении COM+, необходимо сначала включить проверку авторизации на основе ролей для приложения.</span><span class="sxs-lookup"><span data-stu-id="8a154-104">To use role-based security in your COM+ application, you must first enable role-based authorization checking for the application.</span></span> <span data-ttu-id="8a154-105">Это гарантирует, что пользователи, обращающиеся к приложению, проверяются на роль, к которой они принадлежат, прежде чем они смогут выполнять какие-либо действия в приложении.</span><span class="sxs-lookup"><span data-stu-id="8a154-105">This ensures that users who are accessing the application are checked for the role they belong to before they are authorized to do anything in the application.</span></span> <span data-ttu-id="8a154-106">Если проверка авторизации на основе ролей не включена, безопасность на основе ролей для приложения не используется.</span><span class="sxs-lookup"><span data-stu-id="8a154-106">If role-based authorization checking is not enabled, role-based security for the application is not used.</span></span>

<span data-ttu-id="8a154-107">**Включение проверки авторизации на основе ролей**</span><span class="sxs-lookup"><span data-stu-id="8a154-107">**To enable role-based authorization checking**</span></span>

1.  <span data-ttu-id="8a154-108">Щелкните правой кнопкой мыши приложение COM+, для которого включается проверка авторизации на основе ролей, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="8a154-108">Right-click the COM+ application for which you are enabling role-based authorization checking, and then click **Properties**.</span></span>

2.  <span data-ttu-id="8a154-109">В диалоговом окне Свойства приложения перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="8a154-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="8a154-110">В разделе " **авторизация**" установите флажок **Принудительная проверка доступа для этого приложения** . Снятие флажка означает, что для приложения не используется безопасность на основе ролей.</span><span class="sxs-lookup"><span data-stu-id="8a154-110">Under **Authorization**, select the **Enforce access checks for this application** check box; clearing the check box means that role-based security is not used for the application.</span></span>

4.  <span data-ttu-id="8a154-111">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8a154-111">Click **OK**.</span></span>

<span data-ttu-id="8a154-112">Выбранный параметр авторизации вступает в силу при следующем запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="8a154-112">The selected authorization setting takes effect the next time the application is started.</span></span>

 

 



