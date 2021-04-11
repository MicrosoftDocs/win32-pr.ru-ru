---
description: Wavemsp.dll Wave MSP соответствует старым специалистами, написанным до введения MSP в архитектуру потоковой передачи на основе MSP в TAPI 3S.
ms.assetid: 203fcd7b-bf9d-48ad-9452-1f6357c82946
title: Звуковой MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 927a2545fd3da6a5ea186a6716d49222e5efb1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912412"
---
# <a name="wave-msp"></a><span data-ttu-id="cb706-103">Звуковой MSP</span><span class="sxs-lookup"><span data-stu-id="cb706-103">Wave MSP</span></span>

<span data-ttu-id="cb706-104">Wave MSP (Wavemsp.dll) соответствует устаревшим специалистами, написанным до введения MSP в архитектуру потоковой передачи на основе протокола TAPI 3 в формате MSP.</span><span class="sxs-lookup"><span data-stu-id="cb706-104">The Wave MSP (Wavemsp.dll) fits legacy TSPs written prior to the introduction of MSPs into TAPI 3's MSP-based streaming architecture.</span></span> <span data-ttu-id="cb706-105">Некоторые устаревшие специалистами предоставляют идентификаторы устройств, которые были средством управления потоковой передачей в TAPI 2,1.</span><span class="sxs-lookup"><span data-stu-id="cb706-105">Some of the legacy TSPs expose wave device identifiers, which were a means for the application to control streaming under TAPI 2.1.</span></span> <span data-ttu-id="cb706-106">Tapi3.dll использует звуковой MSP для любого TSP, который не имеет своего собственного MSP, но имеет звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="cb706-106">Tapi3.dll uses the Wave MSP for any TSP that does not have its own MSP but that has a wave device.</span></span>

<span data-ttu-id="cb706-107">Звуковой MSP устанавливается вместе с Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cb706-107">The Wave MSP is installed with Windows 2000.</span></span>

 

 



