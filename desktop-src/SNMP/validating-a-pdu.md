---
title: Проверка PDU
description: Если приложение WinSNMP вызывает функцию Снмпсендмсг или Снмпенкодемсг, то реализация Microsoft WinSNMP проверяет допустимость PDU и другие параметры функции.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411228"
---
# <a name="validating-a-pdu"></a><span data-ttu-id="f409c-103">Проверка PDU</span><span class="sxs-lookup"><span data-stu-id="f409c-103">Validating a PDU</span></span>

<span data-ttu-id="f409c-104">Если приложение WinSNMP вызывает функцию [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) или [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , то реализация Microsoft WINSNMP проверяет допустимость PDU и другие параметры функции.</span><span class="sxs-lookup"><span data-stu-id="f409c-104">When the WinSNMP application calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function, the Microsoft WinSNMP implementation verifies the validity of the PDU and the other function parameters.</span></span>

<span data-ttu-id="f409c-105">Значение одного компонента данных PDU (или поля) может быть допустимым по отдельности, но оно может быть недопустимым в сочетании со значениями других полей.</span><span class="sxs-lookup"><span data-stu-id="f409c-105">The value of one PDU data component (or field) can be valid individually, but it may be invalid in combination with values for other fields.</span></span> <span data-ttu-id="f409c-106">Например, если в качестве значения поля **\_ типа PDU** для PDU используется SNMP- \_ PDU \_ или \_ \_ отклика PDU SNMP, то оба поля **\_ состояния ошибки** и **\_ индекса ошибки** должны быть равны нулю.</span><span class="sxs-lookup"><span data-stu-id="f409c-106">For example, unless the **PDU\_type** field of the PDU is SNMP\_PDU\_GETBULK or SNMP\_PDU\_RESPONSE, both the **error\_status** and **error\_index** fields must be equal to zero.</span></span> <span data-ttu-id="f409c-107">Любое другое сочетание значений представляет собой недопустимый PDU.</span><span class="sxs-lookup"><span data-stu-id="f409c-107">Any other value combination constitutes an invalid PDU.</span></span>

<span data-ttu-id="f409c-108">Реализация отклоняет недопустимые PDU и возвращает состояние ошибки СНМПАПИ \_ сбой.</span><span class="sxs-lookup"><span data-stu-id="f409c-108">The implementation rejects invalid PDUs and returns the error status SNMPAPI\_FAILURE.</span></span> <span data-ttu-id="f409c-109">Он устанавливает расширенный код ошибки, равный СНМПАПИ \_ PDU \_ .</span><span class="sxs-lookup"><span data-stu-id="f409c-109">It sets an extended error code equal to SNMPAPI\_PDU\_INVALID.</span></span>

 

 




