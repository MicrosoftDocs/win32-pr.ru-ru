---
title: Настройка программы сжатия и распаковки
description: Настройка программы сжатия и распаковки
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Диспетчер сжатия видео (ВКМ), Настройка компрессоров
- ВКМ (диспетчер сжатия видео), Настройка компрессоров
- Сообщение ICM_CONFIGURE
- Макрос Иккуериконфигуре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986402"
---
# <a name="compressor-and-decompressor-configuration"></a><span data-ttu-id="1bc26-107">Настройка программы сжатия и распаковки</span><span class="sxs-lookup"><span data-stu-id="1bc26-107">Compressor and Decompressor Configuration</span></span>

<span data-ttu-id="1bc26-108">Приложение может автоматически настроить программу сжатия или декомпрессора, а также разрешить пользователю настраивать их.</span><span class="sxs-lookup"><span data-stu-id="1bc26-108">Your application can configure the compressor or decompressor automatically, or it can allow the user to configure them.</span></span> <span data-ttu-id="1bc26-109">Если это целесообразно, разрешите пользователю настроить программу сжатия или распаковку; Это освобождает вас от рассмотрения всех возможностей сжатия или распаковки.</span><span class="sxs-lookup"><span data-stu-id="1bc26-109">If it is practical, allow the user to configure the compressor or decompressor; this frees you from considering all the options for the compressor or decompressor.</span></span>

<span data-ttu-id="1bc26-110">Пользователь может настроить программу сжатия или декомпрессора с помощью диалогового окна конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1bc26-110">The user can configure the compressor or decompressor by using a configuration dialog box.</span></span> <span data-ttu-id="1bc26-111">Можно отправить ICM- [**сообщение \_ настройки**](icm-configure.md) в ВКМ (или использовать макрос [**иккуериконфигуре**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ), чтобы определить, может ли программа сжатия или декомпрессора отображать диалоговое окно конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1bc26-111">You can send the [**ICM\_CONFIGURE**](icm-configure.md) message to VCM (or use the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro) to determine if a compressor or decompressor can display a configuration dialog box.</span></span> <span data-ttu-id="1bc26-112">В этом случае отправьте сообщение ICM \_ Configure (или используйте макрос [**икконфигуре**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ), чтобы отобразить его.</span><span class="sxs-lookup"><span data-stu-id="1bc26-112">If so, send the ICM\_CONFIGURE message (or use the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro) to display it.</span></span>

<span data-ttu-id="1bc26-113">Приложение может отправить сообщения [**ICM- \_ State**](icm-getstate.md) и [**ICM \_ SETSTATE**](icm-setstate.md) (или использовать макросы [**икжетстатесизе**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**икжетстате**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)и [**иксетстате**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) для получения и установки состояния сжатия или распаковки.</span><span class="sxs-lookup"><span data-stu-id="1bc26-113">Your application can send the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages (or use the [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate), and [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macros) to get and set the status for a compressor or decompressor.</span></span> <span data-ttu-id="1bc26-114">Если приложение создает или изменяет состояние, оно должно получить макет данных программы сжатия или декомпрессора перед восстановлением состояния.</span><span class="sxs-lookup"><span data-stu-id="1bc26-114">If your application creates or modifies the status, it must obtain the layout of the compressor or decompressor data before restoring its status.</span></span> <span data-ttu-id="1bc26-115">Кроме того, если приложение получает состояние от программы сжатия или распаковки и использует его для восстановления состояния в последующем сеансе, оно должно обеспечить восстановление только сведений о состоянии, полученных из программы сжатия или распаковки, которая в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="1bc26-115">Alternatively, if your application obtains the status from a compressor or decompressor and uses it to restore the status in a subsequent session, it must ensure that it restores only status information obtained from the compressor or decompressor it is currently using.</span></span>

 

 




