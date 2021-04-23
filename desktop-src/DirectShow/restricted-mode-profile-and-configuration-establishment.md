---
description: Профиль с ограниченным режимом и установка конфигурации
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Профиль с ограниченным режимом и установка конфигурации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416616"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a><span data-ttu-id="d8338-103">Профиль с ограниченным режимом и установка конфигурации</span><span class="sxs-lookup"><span data-stu-id="d8338-103">Restricted Mode Profile and Configuration Establishment</span></span>

<span data-ttu-id="d8338-104">Из-за разнообразных типов данных, которые могут быть декодированы с помощью DirectX ва, и конфигураций с несколькими декодирования, поддерживаемых в DirectX ва для каждого из этих типов данных (например, использование буферов битовый поток в сравнении с остаточным различием узлов и ИДКТ на основе ускорителей с шифрованием и без шифрования каждого соответствующего типа буфера и т. д. Мы считаем, что было бы довольно просто указать уникальный идентификатор GUID для каждого уникального типа данных и декодирования.</span><span class="sxs-lookup"><span data-stu-id="d8338-104">Due to the variety of types of data that can be decoded by DirectX VA, and the multiple decoding configurations supported within DirectX VA for each of these types of data (for example, using bitstream buffers versus host residual difference decoding versus accelerator-based IDCT with and without encryption of each relevant type of buffer, and so on), we believe it would be somewhat ungainly to simply specify a unique GUID for every unique data type and decoding configuration.</span></span> <span data-ttu-id="d8338-105">Это приведет к созданию большого количества идентификаторов GUID (например, если для каждого из них было 16 профилей DirectX ва и 16 конфигураций, для каждого из них потребуется 256 определенных идентификаторов GUID, для хранения которых достаточно 4 КБ памяти.</span><span class="sxs-lookup"><span data-stu-id="d8338-105">This would create a large number of GUIDs (for example, hypothetically if there were 16 profiles of DirectX VA and 16 configurations possible for each, there would need to be 256 defined GUIDs—requiring 4 kilobytes of memory just to hold them all.</span></span> <span data-ttu-id="d8338-106">Эта проблема является самой сложной частью в определении способа преобразования DirectX ва в **иамвидеоакцелератор**, а оставшаяся часть рабочего определения в основном довольно проста.</span><span class="sxs-lookup"><span data-stu-id="d8338-106">This issue is the most difficult part of determining how to map DirectX VA into **IAMVideoAccelerator**, with the remainder of the operational definition mostly being quite straightforward.</span></span> <span data-ttu-id="d8338-107">В результате мы указываем уникальный идентификатор GUID только для каждого типа данных (для каждого профиля с ограниченным режимом) и разрешают связывать дополнительный GUID с каждым типом шифрования.</span><span class="sxs-lookup"><span data-stu-id="d8338-107">As a result, we specify a unique GUID only for each type of data (for each restricted mode profile) and allow an additional GUID to be associated with each type of encryption.</span></span> <span data-ttu-id="d8338-108">Затем конфигурация декодирования устанавливается между декодером и ускорителем подчиненным согласованием на более низком уровне с помощью операций проверки и блокировки для установки конфигураций для каждого типа функции DirectX ва.</span><span class="sxs-lookup"><span data-stu-id="d8338-108">The decoding configuration is then established between the decoder and accelerator by a lower-level subordinate negotiation using probing and locking operations to establish configurations for each type of DirectX VA function.</span></span>

 

 



