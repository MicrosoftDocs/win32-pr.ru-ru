---
description: Синтаксис криптографических сообщений (CMS), производный от PKCS \# 7 версии 1,5, является синтаксисом, используемым для хэширования, цифровой подписи, проверки подлинности и шифрования произвольных сообщений.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Дополнения CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662731"
---
# <a name="cms-additions"></a><span data-ttu-id="f2012-103">Дополнения CMS</span><span class="sxs-lookup"><span data-stu-id="f2012-103">CMS Additions</span></span>

<span data-ttu-id="f2012-104">Синтаксис криптографических сообщений (CMS), производный от PKCS \# 7 версии 1,5, является синтаксисом, используемым для [*хэширования*](../secgloss/h-gly.md), [*цифровой подписи*](../secgloss/d-gly.md), проверки подлинности и шифрования произвольных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2012-104">Cryptographic Message Syntax (CMS), derived from PKCS \#7 version 1.5, is the syntax used to [*hash*](../secgloss/h-gly.md), [*digitally sign*](../secgloss/d-gly.md), authenticate, and encrypt arbitrary messages.</span></span> <span data-ttu-id="f2012-105">Там, где это возможно, обратная совместимость сохраняется; Однако были внесены изменения в соответствии с переносом сертификата атрибута и методами ключевых соглашений для управления ключами.</span><span class="sxs-lookup"><span data-stu-id="f2012-105">Where possible, backward compatibility is preserved; however, changes have been made to accommodate attribute certificate transfer and key agreement techniques for key management.</span></span> <span data-ttu-id="f2012-106">CMS позволяет использовать несколько инкапсуляций, чтобы один конверт инкапсуляции можно было вложить в другой.</span><span class="sxs-lookup"><span data-stu-id="f2012-106">CMS allows multiple encapsulation so that one encapsulation envelope can be nested inside another.</span></span> <span data-ttu-id="f2012-107">Кроме того, одна сторона может подписать ранее инкапсулированные данные. произвольные атрибуты, например время подписи, могут быть подписаны вместе с содержимым сообщения. атрибуты и, такие как [*подписи от других сторон*](../secgloss/c-gly.md), могут быть связаны с сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="f2012-107">Also, one party can digitally sign previously encapsulated data; arbitrary attributes, such as signing time, can be signed along with the message content; and attributes, such as [*countersignatures*](../secgloss/c-gly.md), can be associated with a signature.</span></span> <span data-ttu-id="f2012-108">CMS может поддерживать различные архитектуры управления ключами на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f2012-108">CMS can support a variety of architectures for certificate-based key management.</span></span>

<span data-ttu-id="f2012-109">Для поддержки дополнительных возможностей CMS базовые структуры данных получают новые поля.</span><span class="sxs-lookup"><span data-stu-id="f2012-109">To support additional CMS capabilities, underlying data structures have been given new fields.</span></span> <span data-ttu-id="f2012-110">Также были добавлены новые флаги и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="f2012-110">New flags and parameter values have also been added.</span></span> <span data-ttu-id="f2012-111">Все структуры данных и все интерфейсы API, использующие CMS, имеют 100 процентов обратной совместимости с PKCS \# 7 версии 1,5.</span><span class="sxs-lookup"><span data-stu-id="f2012-111">All data structures and all APIs using CMS are 100 percent backward compatible with PKCS \#7 version 1.5.</span></span>

<span data-ttu-id="f2012-112">К дополнениям относятся добавленные в [оболочку](enveloped-data-additions.md) дополнения и [добавления подписанных данных](signed-data-additions.md).</span><span class="sxs-lookup"><span data-stu-id="f2012-112">Additions include [Enveloped Data Additions](enveloped-data-additions.md) and [Signed Data Additions](signed-data-additions.md).</span></span>

 

 
