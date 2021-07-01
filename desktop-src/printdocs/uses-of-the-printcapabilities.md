---
description: Сведения об использовании PrintCapabilities. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Использование PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119429"
---
# <a name="uses-of-the-printcapabilities"></a><span data-ttu-id="c3735-105">Использование PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c3735-105">Uses of the PrintCapabilities</span></span>

<span data-ttu-id="c3735-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c3735-106">This topic is not current.</span></span> <span data-ttu-id="c3735-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c3735-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c3735-108">PrintCapabilities предназначены для представления настраиваемых атрибутов устройства в виде конструкций "функция-параметр" или конструкции параметров.</span><span class="sxs-lookup"><span data-stu-id="c3735-108">The PrintCapabilities are intended to represent configurable device attributes as either Feature/Option constructs or parameter constructs.</span></span> <span data-ttu-id="c3735-109">Эта информация определяет пространство конфигурации устройства и может использоваться клиентом пользовательского интерфейса для создания пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c3735-109">This information defines the configuration space of the device and can be used by a user interface (UI) client to construct a UI.</span></span> <span data-ttu-id="c3735-110">Ключевые слова схемы Print определяют набор стандартных экземпляров компонентов, экземпляры параметров для стандартных экземпляров компонента и экземпляры Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="c3735-110">The Print Schema Keywords define a set of standard Feature instances, Option instances for the standard Feature instances, and ParameterDef instances.</span></span>

<span data-ttu-id="c3735-111">Функции, параметры и конструкции параметров в PrintCapabilities предназначены для хранения экземпляров свойств или Скоредпроперти, описывающих устройство и поддерживаемых подсистемой диспетчера очереди.</span><span class="sxs-lookup"><span data-stu-id="c3735-111">The Feature/Option or parameter constructs in the PrintCapabilities are intended to hold Property or ScoredProperty instances that describe a device, and that are supported by the spooler subsystem.</span></span> <span data-ttu-id="c3735-112">Эти экземпляры свойств и Скоредпроперти являются общими для клиентов устройства и содержат сведения, предоставляемые функциями Win32 Девкапс.</span><span class="sxs-lookup"><span data-stu-id="c3735-112">These Property and ScoredProperty instances are of general interest to clients of the device, and contain the information that is provided by the Win32 DevCaps functions.</span></span> <span data-ttu-id="c3735-113">Ключевые слова схемы Print определяют набор стандартных свойств и экземпляров Скоредпроперти.</span><span class="sxs-lookup"><span data-stu-id="c3735-113">The Print Schema Keywords define a set of standard Property and ScoredProperty instances.</span></span>

<span data-ttu-id="c3735-114">Следует подчеркнуть, что документ PrintCapabilities предназначен для представления только однозначных данных: данные, которые не зависят от конкретной конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="c3735-114">It should be emphasized that the PrintCapabilities document is intended to represent only single-valued data: data that does not depend on a particular configuration of the device.</span></span> <span data-ttu-id="c3735-115">Документ PrintCapabilities содержит только моментальный снимок данных, зависящих от конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c3735-115">The PrintCapabilities document provides only a snapshot of configuration-dependent data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3735-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c3735-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3735-117">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c3735-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



