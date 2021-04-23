---
description: В дополнение ко всем описанным выше информационным элементам, которые можно было бы указать в структуре QoS, относящейся к ATM при вызове Всаконнект, существует причина, которая может использоваться только в выпуске вызова.
ms.assetid: 258b22d7-b58a-499a-be00-de548578db83
title: Причина
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d2a2864db347183ca42f5458681e4de3ecc6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263077"
---
# <a name="cause"></a><span data-ttu-id="3c559-103">Причина</span><span class="sxs-lookup"><span data-stu-id="3c559-103">Cause</span></span>

<span data-ttu-id="3c559-104">В дополнение ко всем описанным выше информационным элементам, которые можно было бы указать в структуре [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) , относящейся к ATM при вызове [**Всаконнект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), существует причина, которая может использоваться только в выпуске вызова.</span><span class="sxs-lookup"><span data-stu-id="3c559-104">In addition to all the information elements previously described, which could be specified in the ATM-specific [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure while calling [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), there is a Cause IE that can only be used during the call release.</span></span> <span data-ttu-id="3c559-105">При отключении подключения приложения Windows Sockets 2 могут дополнительно указать этот IE в качестве данных отключения в [**всасенддисконнект**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect).</span><span class="sxs-lookup"><span data-stu-id="3c559-105">Upon disconnecting, Windows Sockets 2 applications can optionally specify this IE as the disconnect data in [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect).</span></span> <span data-ttu-id="3c559-106">Удаленная сторона может получить этот IE через [**всареквдисконнект**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) после получения \_ уведомления о закрытии демона.</span><span class="sxs-lookup"><span data-stu-id="3c559-106">The remote party can retrieve this IE through [**WSARecvDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvdisconnect) after receiving the FD\_CLOSE notification.</span></span>

``` syntax
#include <windows.h>

/* 
 *  values used for the Location field in struct ATM_CAUSE_IE
 */
#define CAUSE_LOC_USER                      0x00
#define CAUSE_LOC_PRIVATE_LOCAL             0x01
#define CAUSE_LOC_PUBLIC_LOCAL              0x02
#define CAUSE_LOC_TRANSIT_NETWORK           0x03
#define CAUSE_LOC_PUBLIC_REMOTE             0x04
#define CAUSE_LOC_PRIVATE_REMOTE            0x05
#define CAUSE_LOC_INTERNATIONAL_NETWORK     0x06
#define CAUSE_LOC_BEYOND_INTERWORKING       0x0A

/* 
 *  values used for the Cause field in struct ATM_CAUSE_IE
 */
#define CAUSE_UNALLOCATED_NUMBER                0x01
#define CAUSE_NO_ROUTE_TO_TRANSIT_NETWORK       0x02
#define CAUSE_NO_ROUTE_TO_DESTINATION           0x03
#define CAUSE_VPI_VCI_UNACCEPTABLE              0x0A
#define CAUSE_NORMAL_CALL_CLEARING              0x10
#define CAUSE_USER_BUSY                         0x11
#define CAUSE_NO_USER_RESPONDING                0x12
#define CAUSE_CALL_REJECTED                     0x15
#define CAUSE_NUMBER_CHANGED                    0x16
#define CAUSE_USER_REJECTS_CLIR                 0x17
#define CAUSE_DESTINATION_OUT_OF_ORDER          0x1B
#define CAUSE_INVALID_NUMBER_FORMAT             0x1C
#define CAUSE_STATUS_ENQUIRY_RESPONSE           0x1E
#define CAUSE_NORMAL_UNSPECIFIED                0x1F
#define CAUSE_VPI_VCI_UNAVAILABLE               0x23
#define CAUSE_NETWORK_OUT_OF_ORDER              0x26
#define CAUSE_TEMPORARY_FAILURE                 0x29
#define CAUSE_ACCESS_INFORMAION_DISCARDED       0x2B
#define CAUSE_NO_VPI_VCI_AVAILABLE              0x2D
#define CAUSE_RESOURCE_UNAVAILABLE              0x2F
#define CAUSE_QOS_UNAVAILABLE                   0x31
#define CAUSE_USER_CELL_RATE_UNAVAILABLE        0x33
#define CAUSE_BEARER_CAPABILITY_UNAUTHORIZED    0x39
#define CAUSE_BEARER_CAPABILITY_UNAVAILABLE     0x3A
#define CAUSE_OPTION_UNAVAILABLE                0x3F
#define CAUSE_BEARER_CAPABILITY_UNIMPLEMENTED   0x41
#define CAUSE_UNSUPPORTED_TRAFFIC_PARAMETERS    0x49
#define CAUSE_INVALID_CALL_REFERENCE            0x51
#define CAUSE_CHANNEL_NONEXISTENT               0x52
#define CAUSE_INCOMPATIBLE_DESTINATION          0x58
#define CAUSE_INVALID_ENDPOINT_REFERENCE        0x59
#define CAUSE_INVALID_TRANSIT_NETWORK_SELECTION 0x5B
#define CAUSE_TOO_MANY_PENDING_ADD_PARTY        0x5C
#define CAUSE_AAL_PARAMETERS_UNSUPPORTED        0x5D
#define CAUSE_MANDATORY_IE_MISSING              0x60
#define CAUSE_UNIMPLEMENTED_MESSAGE_TYPE        0x61
#define CAUSE_UNIMPLEMENTED_IE                  0x63
#define CAUSE_INVALID_IE_CONTENTS               0x64
#define CAUSE_INVALID_STATE_FOR_MESSAGE         0x65
#define CAUSE_RECOVERY_ON_TIMEOUT               0x66
#define CAUSE_INCORRECT_MESSAGE_LENGTH          0x68
#define CAUSE_PROTOCOL_ERROR                    0x6F

/* 
 *  values used for the Condition portion of the Diagnostics field
 *  in struct ATM_CAUSE_IE, for certain Cause values
 */
#define CAUSE_COND_UNKNOWN                  0x00
#define CAUSE_COND_PERMANENT                0x01
#define CAUSE_COND_TRANSIENT                0x02

/* 
 *  values used for the Rejection Reason portion of the Diagnostics field
 *  in struct ATM_CAUSE_IE, for certain Cause values
 */
#define CAUSE_REASON_USER                   0x00
#define CAUSE_REASON_IE_MISSING             0x04
#define CAUSE_REASON_IE_INSUFFICIENT        0x08

/* 
 *  values used for the P-U flag of the Diagnostics field
 *  in struct ATM_CAUSE_IE, for certain Cause values
 */
#define CAUSE_PU_PROVIDER                   0x00
#define CAUSE_PU_USER                       0x08

/* 
 *  values used for the N-A flag of the Diagnostics field
 *  in struct ATM_CAUSE_IE, for certain Cause values
 */
#define CAUSE_NA_NORMAL                     0x00
#define CAUSE_NA_ABNORMAL                   0x04

typedef struct {
    UCHAR Location;
    UCHAR Cause;
    UCHAR DiagnosticsLength;
    UCHAR Diagnostics[4];
} ATM_CAUSE_IE;
```

 

 



