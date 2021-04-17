---
description: Для делегирования учетных данных протокол CredSSP необходимо указать, к каким серверам можно делегировать.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Параметры групповая политика CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650882"
---
# <a name="credssp-group-policy-settings"></a><span data-ttu-id="f49ec-103">Параметры групповая политика CredSSP</span><span class="sxs-lookup"><span data-stu-id="f49ec-103">CredSSP Group Policy Settings</span></span>

<span data-ttu-id="f49ec-104">Для делегирования учетных данных [протокол CredSSP](credential-security-support-provider.md) необходимо указать, к каким серверам можно делегировать.</span><span class="sxs-lookup"><span data-stu-id="f49ec-104">For [Credential Security Support Provider protocol (CredSSP)](credential-security-support-provider.md) to delegate credentials, you must specify which servers can be delegated to.</span></span> <span data-ttu-id="f49ec-105">Чтобы указать эти серверы, измените параметры в редакторе групповая политика (ГПЕ) оснастку консоли управления (MMC).</span><span class="sxs-lookup"><span data-stu-id="f49ec-105">To specify those servers, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in.</span></span> <span data-ttu-id="f49ec-106">Параметры ГПЕ, управляющие делегированием, находятся в разделе **Конфигурация компьютера \| Административные шаблоны \| \| Делегирование системных учетных данных**.</span><span class="sxs-lookup"><span data-stu-id="f49ec-106">The GPE settings that control delegation are under **Computer Configuration \| Administrative Templates \| System \| Credentials Delegation**.</span></span>

> [!Caution]  
> <span data-ttu-id="f49ec-107">Это не ограниченное делегирование.</span><span class="sxs-lookup"><span data-stu-id="f49ec-107">This is not constrained delegation.</span></span> <span data-ttu-id="f49ec-108">CredSSP передает полные учетные данные пользователя на сервер без каких бы то ни было ограничений.</span><span class="sxs-lookup"><span data-stu-id="f49ec-108">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="f49ec-109">Параметры групповой политики управляют делегированием следующих типов учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f49ec-109">Group policy settings control delegation of the following types of credentials.</span></span>



| <span data-ttu-id="f49ec-110">Тип учетных данных</span><span class="sxs-lookup"><span data-stu-id="f49ec-110">Credentials Type</span></span>                                                                                                                                 | <span data-ttu-id="f49ec-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f49ec-111">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f49ec-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Учетные данные по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f49ec-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Default credentials</span></span><br/> | <span data-ttu-id="f49ec-113">Учетные данные, полученные при первом входе пользователя в Windows.</span><span class="sxs-lookup"><span data-stu-id="f49ec-113">The credentials obtained when the user first logs on to Windows.</span></span><br/>                   |
| <span data-ttu-id="f49ec-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Новые учетные данные</span><span class="sxs-lookup"><span data-stu-id="f49ec-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Fresh credentials</span></span><br/>         | <span data-ttu-id="f49ec-115">Учетные данные, на которые запрашивается пользователь при выполнении приложения.</span><span class="sxs-lookup"><span data-stu-id="f49ec-115">The credentials that the user is prompted for when executing an application.</span></span><br/>       |
| <span data-ttu-id="f49ec-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Сохраненные учетные данные</span><span class="sxs-lookup"><span data-stu-id="f49ec-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Saved credentials</span></span><br/>         | <span data-ttu-id="f49ec-117">Учетные данные, сохраненные с помощью [диспетчера учетных данных](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="f49ec-117">The credentials that are saved using [Credential Manager](credential-manager.md).</span></span><br/> |



 

<span data-ttu-id="f49ec-118">Чтобы включить сервер в категорию, связанную с определенным параметром групповой политики, добавьте [*имя участника-службы*](/windows/desktop/SecGloss/s-gly) (SPN) этого сервера в список серверов для этого параметра групповой политики.</span><span class="sxs-lookup"><span data-stu-id="f49ec-118">To include a server in the category associated with a particular group policy setting, add the [*Service Principal Name*](/windows/desktop/SecGloss/s-gly) (SPN) of that server to the list of servers for that group policy setting.</span></span> <span data-ttu-id="f49ec-119">Имя субъекта-службы может содержать один подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="f49ec-119">The SPN can contain a single wildcard character.</span></span>

 

