---
title: Потерянный дескриптор D1103
ms.assetid: 9bb08cd6-104a-4168-b14e-3caec1679388
description: Интерфейс был создан, но не был освобожден.
keywords:
- D1103 утечка дескриптора Direct2D
topic_type:
- apiref
api_name:
- D1103 Leaked Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cc4b4e43f94bd4ceb5d7a2518879c69bd3ecf8f3
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105658173"
---
# <a name="d1103-leaked-handle"></a><span data-ttu-id="63cf2-104">D1103: утечка дескриптора</span><span class="sxs-lookup"><span data-stu-id="63cf2-104">D1103: Leaked Handle</span></span>

<span data-ttu-id="63cf2-105">Интерфейс интерфейса \[  \] был создан, но не был освобожден.</span><span class="sxs-lookup"><span data-stu-id="63cf2-105">An interface \[*interface*\] was created but not released.</span></span>

## <a name="placeholders"></a><span data-ttu-id="63cf2-106">Заполнители</span><span class="sxs-lookup"><span data-stu-id="63cf2-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="63cf2-107"><span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="63cf2-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="63cf2-108">Адрес интерфейса.</span><span class="sxs-lookup"><span data-stu-id="63cf2-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="63cf2-109">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="63cf2-109">Possible Causes</span></span>

<span data-ttu-id="63cf2-110">Недопустимое использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63cf2-110">Invalid resource usage.</span></span> <span data-ttu-id="63cf2-111">Приложению не удается освободить интерфейс, когда он больше не используется.</span><span class="sxs-lookup"><span data-stu-id="63cf2-111">An application fails to release an interface when it is no longer in use.</span></span>

 

 




