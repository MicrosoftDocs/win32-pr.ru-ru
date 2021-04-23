---
title: Инфраструктура диагностики сети
description: Инфраструктура диагностики сети (NDF) предоставляет разработчикам компонентов и приложений возможность упростить устранение неполадок в сети для пользователей.
ms.assetid: 61dfb66b-4bc6-43a9-ad61-698f5cd67f4a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0342ee4cb285f0a0f1c76c74b3bdc5b412b07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067681"
---
# <a name="network-diagnostics-framework"></a><span data-ttu-id="b64c9-103">Инфраструктура диагностики сети</span><span class="sxs-lookup"><span data-stu-id="b64c9-103">Network Diagnostics Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="b64c9-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="b64c9-104">Purpose</span></span>

<span data-ttu-id="b64c9-105">Инфраструктура диагностики сети (NDF) предоставляет разработчикам компонентов и приложений возможность упростить устранение неполадок в сети для пользователей.</span><span class="sxs-lookup"><span data-stu-id="b64c9-105">The Network Diagnostics Framework (NDF) provides a way for component and application developers to simplify network troubleshooting for users.</span></span> <span data-ttu-id="b64c9-106">Пользователи могут попытаться диагностировать и устранить проблему с сетью с помощью одного средства устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="b64c9-106">Users can attempt to diagnose and repair a network problem using a single troubleshooting tool.</span></span>

<span data-ttu-id="b64c9-107">Корпорация Майкрософт предоставляет вспомогательные классы NDF, некоторые из которых являются расширяемыми, чтобы разработчики могли создавать модули устранения неполадок, называемые вспомогательными расширениями классов, чтобы обеспечить более подробную диагностику конкретных программных или аппаратных компонентов.</span><span class="sxs-lookup"><span data-stu-id="b64c9-107">Microsoft provides NDF helper classes, some of which are extensible so that developers can create troubleshooting units called helper class extensions to provide more detailed diagnoses specific to particular software or hardware components.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b64c9-108">Где применимо</span><span class="sxs-lookup"><span data-stu-id="b64c9-108">Where applicable</span></span>

<span data-ttu-id="b64c9-109">NDF может использоваться программным обеспечением любого поставщика, которое зависит от сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="b64c9-109">NDF can be used by any vendor's software which relies on network connectivity.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b64c9-110">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="b64c9-110">Developer audience</span></span>

<span data-ttu-id="b64c9-111">API NDF предназначен для разработчиков C/C++.</span><span class="sxs-lookup"><span data-stu-id="b64c9-111">The NDF API is designed for C/C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b64c9-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="b64c9-112">Run-time requirements</span></span>

<span data-ttu-id="b64c9-113">NDF доступен для компьютеров под управлением Windows Vista, Windows Server 2008 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b64c9-113">NDF is available for computers running Windows Vista, Windows Server 2008, or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b64c9-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b64c9-114">In this section</span></span>



| <span data-ttu-id="b64c9-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="b64c9-115">Topic</span></span>                                                                       | <span data-ttu-id="b64c9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b64c9-116">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b64c9-117">О NDF</span><span class="sxs-lookup"><span data-stu-id="b64c9-117">About NDF</span></span>](about-ndf.md)<br/>                                       | <span data-ttu-id="b64c9-118">Общие сведения о технологии NDF.</span><span class="sxs-lookup"><span data-stu-id="b64c9-118">Provides a general summary of the NDF technology.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="b64c9-119">Использование NDF</span><span class="sxs-lookup"><span data-stu-id="b64c9-119">Using NDF</span></span>](using-ndf.md)<br/>                                       | <span data-ttu-id="b64c9-120">Содержит сведения и примеры использования функций NDF, а также способы расширения этих функций.</span><span class="sxs-lookup"><span data-stu-id="b64c9-120">Provides information and examples on using NDF functionality, as well as how to extend this functionality.</span></span><br/>                                                                                    |
| [<span data-ttu-id="b64c9-121">Справочник по NDF</span><span class="sxs-lookup"><span data-stu-id="b64c9-121">NDF Reference</span></span>](ndf-reference.md)<br/>                               | <span data-ttu-id="b64c9-122">Предоставляет сведения о перечислениях, функциях, интерфейсах и структурах, поддерживающих использование NDF, а также сведения о расширяемых вспомогательных классах, предоставляемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b64c9-122">Provides information about enumerations, functions, interfaces, and structures that support the use of NDF, as well as information about the extensible helper classes provided by Microsoft.</span></span><br/> |
| [<span data-ttu-id="b64c9-123">Трассировка сети в Windows 7</span><span class="sxs-lookup"><span data-stu-id="b64c9-123">Network Tracing in Windows 7</span></span>](network-tracing-in-windows-7.md)<br/> | <span data-ttu-id="b64c9-124">Обсуждение трассировки сети и средств, используемых для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="b64c9-124">Discusses network tracing and tools to use for troubleshooting.</span></span><br/>                                                                                                                               |



 

 

 





