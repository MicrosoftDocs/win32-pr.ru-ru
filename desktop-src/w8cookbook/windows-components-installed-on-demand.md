---
title: Компоненты Windows, установленные по запросу
description: Компоненты Windows, установленные по запросу
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104070752"
---
# <a name="windows-components-installed-on-demand"></a><span data-ttu-id="e452d-103">Компоненты Windows, установленные по запросу</span><span class="sxs-lookup"><span data-stu-id="e452d-103">Windows components installed on demand</span></span>

## <a name="platform"></a><span data-ttu-id="e452d-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="e452d-104">Platform</span></span>

<span data-ttu-id="e452d-105">**Клиенты —** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e452d-105">**Clients -** Windows 8.1</span></span>  







## <a name="description"></a><span data-ttu-id="e452d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e452d-106">Description</span></span>

<span data-ttu-id="e452d-107">Два компонента Windows будут установлены по запросу в Windows 8.1: DirectPlay и NTVDM.</span><span class="sxs-lookup"><span data-stu-id="e452d-107">Two Windows components will be installed on demand in Windows 8.1: DirectPlay and NTVDM.</span></span> <span data-ttu-id="e452d-108">Эти компоненты перечислены в необязательных компонентах в узле "устаревшие компоненты".</span><span class="sxs-lookup"><span data-stu-id="e452d-108">These components are listed within Optional Components under the “Legacy Components” node.</span></span> <span data-ttu-id="e452d-109">Эти компоненты устанавливаются локально в составе операционной системы и сжимаются как дополнительные компоненты.</span><span class="sxs-lookup"><span data-stu-id="e452d-109">These components are installed locally as part of the operating system, and compressed as optional components.</span></span> <span data-ttu-id="e452d-110">Когда приложение обращается или вызывает один из этих компонентов (обычно при первом запуске приложения), установка активируется автоматически.</span><span class="sxs-lookup"><span data-stu-id="e452d-110">When an app references or calls one of these components (usually at first launch of the app), installation is triggered automatically.</span></span> <span data-ttu-id="e452d-111">Пользователи будут уведомлены о том, что компонент будет установлен, и они должны подтвердить действие для продолжения.</span><span class="sxs-lookup"><span data-stu-id="e452d-111">Users will be notified that the component will be installed, and they must confirm the action in order to proceed.</span></span> <span data-ttu-id="e452d-112">Для этого требуется повышение прав, если пользователь не является администратором.</span><span class="sxs-lookup"><span data-stu-id="e452d-112">Elevation is required for this to succeed if the user is not an administrator.</span></span> <span data-ttu-id="e452d-113">После первоначальной установки пользователю не нужно выполнять никакие другие действия для повторного использования компонента.</span><span class="sxs-lookup"><span data-stu-id="e452d-113">After the initial installation, the user does not need to perform any other actions to use the component again.</span></span>

## <a name="manifestation"></a><span data-ttu-id="e452d-114">Проявление</span><span class="sxs-lookup"><span data-stu-id="e452d-114">Manifestation</span></span>

<span data-ttu-id="e452d-115">Когда приложение ссылается на устаревший компонент или вызывает его в дополнительных компонентах (при первом запуске), приложение будет приостановлено и откроется диалоговое окно "компонент по запросу", запрашивающее разрешение пользователя на установку компонента.</span><span class="sxs-lookup"><span data-stu-id="e452d-115">When an app references or calls a legacy component in optional components (at first launch), the app will be suspended and the Feature on Demand dialog will open, requesting user permission to install the component.</span></span> <span data-ttu-id="e452d-116">Если пользователь нажимаем кнопку "ОК", они также могут увидеть запрос на повышение прав, когда они должны ввести свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e452d-116">If users click OK, they may also see an elevation prompt where they must enter their credentials.</span></span> <span data-ttu-id="e452d-117">Затем компонент будет установлен и приложение будет возобновлено.</span><span class="sxs-lookup"><span data-stu-id="e452d-117">The component will then be installed and the app will resume.</span></span>

## <a name="mitigation"></a><span data-ttu-id="e452d-118">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="e452d-118">Mitigation</span></span>

<span data-ttu-id="e452d-119">Чтобы эти компоненты не открывались в интерфейсе пользователя по запросу, можно предварительно установить DirectPlay и NTVDM с помощью DISM или пользовательского интерфейса дополнительных компонентов.</span><span class="sxs-lookup"><span data-stu-id="e452d-119">To keep the Features on Demand UI from opening, you can pre-install DirectPlay and NTVDM using DISM or the Optional Components UI.</span></span>

## <a name="solution"></a><span data-ttu-id="e452d-120">Решение</span><span class="sxs-lookup"><span data-stu-id="e452d-120">Solution</span></span>

<span data-ttu-id="e452d-121">Настоятельно рекомендуется избегать ссылок или вызова компонентов, которые были указаны как устаревшие необязательные компоненты в Windows в будущих версиях приложения.</span><span class="sxs-lookup"><span data-stu-id="e452d-121">You are strongly encouraged to avoid referencing or calling components that have been listed as Legacy Optional Components in Windows in future versions of your app.</span></span> <span data-ttu-id="e452d-122">Устаревшие необязательные компоненты содержат только старые, менее используемые компоненты, которые могут вызвать проблемы с производительностью и безопасностью пользователей.</span><span class="sxs-lookup"><span data-stu-id="e452d-122">Legacy Optional Components will only include older, lesser-used components that could potentially cause performance and security issues for users.</span></span>

## <a name="tests"></a><span data-ttu-id="e452d-123">Тесты</span><span class="sxs-lookup"><span data-stu-id="e452d-123">Tests</span></span>

<span data-ttu-id="e452d-124">Для обеспечения совместимости не требуется никаких дополнительных тестовых размещений.</span><span class="sxs-lookup"><span data-stu-id="e452d-124">No additional test accommodations are necessary for compatibility.</span></span> <span data-ttu-id="e452d-125">Важно помнить, что это диалоговое окно появляется при вызове или ссылке на дополнительный компонент, и эта установка требует повышения прав.</span><span class="sxs-lookup"><span data-stu-id="e452d-125">It is important to be aware that this dialog will appear when the optional component is called or referenced, and this installation requires elevation.</span></span>

 

 




