---
description: Определяет пару из 802,11 алгоритмов проверки подлинности и шифров, которые могут быть включены одновременно на станции 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Структура DOT11_AUTH_CIPHER_PAIR (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683669"
---
# <a name="dot11_auth_cipher_pair-structure"></a><span data-ttu-id="555f4-103">\_ \_ Структура пары шифров для проверки подлинности DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="555f4-103">DOT11\_AUTH\_CIPHER\_PAIR structure</span></span>

<span data-ttu-id="555f4-104">Структура **\_ \_ \_ пары шифров** для проверки подлинности DOT11 определяет пару из 802,11 алгоритмов шифрования и шифров, которые могут быть включены одновременно на станции 802,11.</span><span class="sxs-lookup"><span data-stu-id="555f4-104">The **DOT11\_AUTH\_CIPHER\_PAIR** structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.</span></span>

## <a name="syntax"></a><span data-ttu-id="555f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="555f4-105">Syntax</span></span>


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a><span data-ttu-id="555f4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="555f4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="555f4-107">**аусалгоид**</span><span class="sxs-lookup"><span data-stu-id="555f4-107">**AuthAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="555f4-108">Алгоритм проверки подлинности, использующий перечислимый тип [**\_ \_ алгоритма проверки**](dot11-auth-algorithm.md) подлинности DOT11.</span><span class="sxs-lookup"><span data-stu-id="555f4-108">An authentication algorithm that uses a [**DOT11\_AUTH\_ALGORITHM**](dot11-auth-algorithm.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="555f4-109">**Цифералгоид**</span><span class="sxs-lookup"><span data-stu-id="555f4-109">**CipherAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="555f4-110">Алгоритм шифрования, использующий перечислимый тип [**\_ \_ алгоритма шифрования DOT11**](dot11-cipher-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="555f4-110">A cipher algorithm that uses a [**DOT11\_CIPHER\_ALGORITHM**](dot11-cipher-algorithm.md) enumerated type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="555f4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="555f4-111">Remarks</span></span>

<span data-ttu-id="555f4-112">\_ \_ Пара шифров шифрования DOT11 \_ определяет алгоритм проверки подлинности и шифрования, который можно включить совместно для сетевых подключений "базовый набор служб (BSS)".</span><span class="sxs-lookup"><span data-stu-id="555f4-112">The DOT11\_AUTH\_CIPHER\_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="555f4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="555f4-113">Requirements</span></span>



| <span data-ttu-id="555f4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="555f4-114">Requirement</span></span> | <span data-ttu-id="555f4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="555f4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="555f4-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="555f4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="555f4-117">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="555f4-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="555f4-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="555f4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="555f4-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="555f4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="555f4-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="555f4-120">Redistributable</span></span><br/>          | <span data-ttu-id="555f4-121">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="555f4-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="555f4-122">Header</span><span class="sxs-lookup"><span data-stu-id="555f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="555f4-123"><dt>Влантипес. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="555f4-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="555f4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="555f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555f4-125">**\_Алгоритм проверки подлинности DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="555f4-125">**DOT11\_AUTH\_ALGORITHM**</span></span>](dot11-auth-algorithm.md)
</dt> <dt>

[<span data-ttu-id="555f4-126">**\_Алгоритм шифрования \_ DOT11**</span><span class="sxs-lookup"><span data-stu-id="555f4-126">**DOT11\_CIPHER\_ALGORITHM**</span></span>](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




