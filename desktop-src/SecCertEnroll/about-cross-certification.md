---
description: Перекрестная сертификация позволяет сущностям в одной инфраструктуре открытых ключей (PKI) доверять сущностям в другой PKI.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Перекрестная сертификация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265639"
---
# <a name="cross-certification"></a><span data-ttu-id="23f92-103">Перекрестная сертификация</span><span class="sxs-lookup"><span data-stu-id="23f92-103">Cross Certification</span></span>

<span data-ttu-id="23f92-104">Перекрестная сертификация позволяет сущностям в одной инфраструктуре открытых ключей (PKI) доверять сущностям в другой PKI.</span><span class="sxs-lookup"><span data-stu-id="23f92-104">Cross certification enables entities in one public key infrastructure (PKI) to trust entities in another PKI.</span></span> <span data-ttu-id="23f92-105">Это отношение взаимного доверия обычно поддерживается соглашением о перекрестной сертификации между центрами сертификации (CAs) в каждой инфраструктуре PKI.</span><span class="sxs-lookup"><span data-stu-id="23f92-105">This mutual trust relationship is typically supported by a cross-certification agreement between the certification authorities (CAs) in each PKI.</span></span> <span data-ttu-id="23f92-106">Соглашение устанавливает обязанности и ответственность каждой стороны.</span><span class="sxs-lookup"><span data-stu-id="23f92-106">The agreement establishes the responsibilities and liability of each party.</span></span>

<span data-ttu-id="23f92-107">Взаимное отношение доверия между двумя центрами сертификации требует, чтобы каждый ЦС выдавал сертификат другому, чтобы установить связь в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="23f92-107">A mutual trust relationship between two CAs requires that each CA issue a certificate to the other to establish the relationship in both directions.</span></span> <span data-ttu-id="23f92-108">Путь доверия не является иерархическим (ни один из управляющих центров сертификации не является подчиненным другим), хотя отдельные PKI могут быть иерархиями сертификатов.</span><span class="sxs-lookup"><span data-stu-id="23f92-108">The path of trust is not hierarchal (neither of the governing CAs is subordinate to the other) although the separate PKIs may be certificate hierarchies.</span></span> <span data-ttu-id="23f92-109">После того как два ЦС установлены и указали условия доверия и выдавали сертификаты друг другу, сущности в отдельном PKI могут взаимодействовать с политиками, указанными в сертификатах.</span><span class="sxs-lookup"><span data-stu-id="23f92-109">After two CAs have established and specified the terms of trust and issued certificates to each other, entities within the separate PKIs can interact subject to the policies specified in the certificates.</span></span>

![Схема перекрестной сертификации](images/cross-certification.png)

## <a name="related-topics"></a><span data-ttu-id="23f92-111">См. также</span><span class="sxs-lookup"><span data-stu-id="23f92-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23f92-112">Модели доверия</span><span class="sxs-lookup"><span data-stu-id="23f92-112">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



