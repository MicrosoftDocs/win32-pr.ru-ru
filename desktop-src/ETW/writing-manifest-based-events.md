---
description: Прежде чем можно будет записывать события в сеанс трассировки, необходимо зарегистрировать поставщик.
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: Написание событий на основе манифеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a1817defe85e68860d8a628a2d3275034ce285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154926"
---
# <a name="writing-manifest-based-events"></a>Написание событий на основе манифеста

Прежде чем можно будет записывать события в сеанс трассировки, необходимо зарегистрировать поставщик. Регистрация поставщика сообщает ETW о том, что поставщик готов к записи событий в сеанс трассировки. Процесс может зарегистрировать до 1 024 идентификаторов GUID поставщика. Однако количество поставщиков, которые регистрируется процессом, должно быть ограничено одним или двумя.

**До Windows Vista:** Количество поставщиков, которые может зарегистрировать процесс, не ограничено.

Чтобы зарегистрировать поставщик на основе манифеста, вызовите функцию [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) . Функция регистрирует GUID поставщика и определяет необязательный обратный вызов, который ETW вызывает, когда контроллер включает или отключает поставщик.

Перед завершением работы поставщика вызовите функцию [**евентунрегистер**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) , чтобы удалить регистрацию поставщика из ETW. Функция [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) возвращает маркер регистрации, передаваемый в функцию **евентунрегистер** .

Поставщики [на основе манифеста](about-event-tracing.md) не должны реализовывать функцию [**енаблекаллбакк**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) для получения уведомлений, когда сеанс включает или отключает поставщик. Обратный вызов является необязательным и используется в информационных целях. При регистрации поставщика не нужно указывать или реализовывать обратный вызов. Поставщик на основе манифеста может просто записывать события, и ETW будет решать, регистрируется ли событие в сеансе трассировки. Если событие требует выполнения сложной работы для создания данных события, может потребоваться сначала вызвать функцию [**евентенаблед**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) или [**евентпровидеренаблед**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) , чтобы убедиться, что событие будет записано в сеанс перед выполнением работы.

Как правило, функция обратного вызова реализуется, если поставщик требует, чтобы контроллер продавал определенные поставщиком данные фильтра (см. параметр *FilterData* [**енаблекаллбакк**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) поставщику, или поставщик использует сведения о контексте, указанные при его регистрации (см. параметр *CallbackContext* в [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).

Поставщики [на основе манифеста](about-event-tracing.md) вызывают функцию [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) или [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) для записи событий в сеанс. Если данные события являются строкой или если не определен манифест для поставщика, а данные события представляют собой одну строку, вызовите функцию [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) для записи события. Для данных событий, содержащих числовые или сложные типы данных, вызовите функцию [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) , чтобы зарегистрировать событие.

В следующем примере показано, как подготовить данные события для написания с помощью функции [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) . В этом примере указываются события, определенные при [публикации схемы событий для поставщика на основе манифеста](publishing-your-event-schema-for-a-manifest-base-provider.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <evntprov.h>
#include "provider.h"  // Generated from manifest

#define SUNDAY     0X1
#define MONDAY     0X2
#define TUESDAY    0X4
#define WEDNESDAY  0X8
#define THURSDAY   0X10
#define FRIDAY     0X20
#define SATURDAY   0X40

enum TRANSFER_TYPE {
  Download = 1,
  Upload,
  UploadReply
};

#define MAX_NAMEDVALUES          5  // Maximum array size
#define MAX_PAYLOAD_DESCRIPTORS  9 + (2 * MAX_NAMEDVALUES)

typedef struct _namedvalue {
  LPWSTR name;
  USHORT value;
} NAMEDVALUE, *PNAMEDVALUE;

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    REGHANDLE RegistrationHandle = NULL; 
    EVENT_DATA_DESCRIPTOR Descriptors[MAX_PAYLOAD_DESCRIPTORS]; 
    DWORD i = 0;

    // Data to load into event descriptors

    USHORT Scores[3] = {45, 63, 21};
    ULONG pImage = (ULONG)&Scores;
    DWORD TransferType = Upload;
    DWORD Day = MONDAY | TUESDAY;
    LPWSTR Path = L"c:\\path\\folder\\file.ext";
    BYTE Cert[11] = {0x2, 0x4, 0x8, 0x10, 0x20, 0x30, 0x40, 0x50, 0x60, 0x0, 0x1};
    PBYTE Guid = (PBYTE) &ProviderGuid;
    USHORT ArraySize = MAX_NAMEDVALUES;
    BOOL IsLocal = TRUE;
    NAMEDVALUE NamedValues[MAX_NAMEDVALUES] = { 
        {L"Bill", 1},
        {L"Bob", 2},
        {L"William", 3},
        {L"Robert", 4},
        {L"", 5}
        };

    status = EventRegister(
        &ProviderGuid,      // GUID that identifies the provider
        NULL,               // Callback not used
        NULL,               // Context noot used
        &RegistrationHandle // Used when calling EventWrite and EventUnregister
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EventRegister failed with %lu\n", status);
        goto cleanup;
    }
  
    // Load the array of data descriptors for the TransferEvent event. 
    // Add the data to the array in the order of the <data> elements
    // defined in the event's template. 
   
    EventDataDescCreate(&Descriptors[i++], &pImage, sizeof(ULONG));
    EventDataDescCreate(&Descriptors[i++], Scores, sizeof(Scores));
    EventDataDescCreate(&Descriptors[i++], Guid, sizeof(GUID));
    EventDataDescCreate(&Descriptors[i++], Cert, sizeof(Cert));
    EventDataDescCreate(&Descriptors[i++], &IsLocal, sizeof(BOOL));
    EventDataDescCreate(&Descriptors[i++], Path, (ULONG)(wcslen(Path) + 1) * sizeof(WCHAR));
    EventDataDescCreate(&Descriptors[i++], &ArraySize, sizeof(USHORT));

    // If your event contains a structure, you should write each member
    // of the structure separately. If the structure contained integral data types
    // such as DWORDs and the data types were aligned on an 8-byte boundary, you 
    // could use the following call to write the structure, however, you are 
    // encouraged to write the members separately.
    //
    // EventDataDescCreate(&EvtData, struct, sizeof(struct));
    //
    // Because the array of structures in this example contains both strings 
    // and numbers, you must write each member of the structure separately.

    for (int j = 0; j < MAX_NAMEDVALUES; j++)
    {
        EventDataDescCreate(&Descriptors[i++], NamedValues[j].name, (ULONG)(wcslen(NamedValues[j].name)+1) * sizeof(WCHAR) );
        EventDataDescCreate(&Descriptors[i++], &(NamedValues[j].value), sizeof(USHORT) );
    }

    EventDataDescCreate(&Descriptors[i++], &Day, sizeof(DWORD));
    EventDataDescCreate(&Descriptors[i++], &TransferType, sizeof(DWORD));

    // Write the event. You do not have to verify if your provider is enabled before
    // writing the event. ETW will write the event to any session that enabled
    // the provider. If no session enabled the provider, the event is not 
    // written. If you need to perform extra work to write an event that you
    // would not otherwise do, you may want to call the EventEnabled function
    // before performing the extra work. The EventEnabled function tells you if a
    // session has enabled your provider, so you know if you need to perform the 
    // extra work or not.

    status = EventWrite(
        RegistrationHandle,              // From EventRegister
        &TransferEvent,                  // EVENT_DESCRIPTOR generated from the manifest
        (ULONG)MAX_PAYLOAD_DESCRIPTORS,  // Size of the array of EVENT_DATA_DESCRIPTORs
        &Descriptors[0]                  // Array of descriptors that contain the event data
        );

    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"EventWrite failed with 0x%x", status);
    }

cleanup:

    EventUnregister(RegistrationHandle);
}
```



При компиляции манифеста (см. раздел [Компиляция манифеста инструментирования](../wes/compiling-an-instrumentation-manifest.md)), который использовался в приведенном выше примере, он создает следующий заголовочный файл (указанный в примере выше).


```C++
//**********************************************************************`
//* This is an include file generated by Message Compiler.             *`
//*                                                                    *`
//* Copyright (c) Microsoft Corporation. All Rights Reserved.          *`
//**********************************************************************`
#pragma once
//+
// Provider Microsoft-Windows-ETWProvider Event Count 1
//+
EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};
//
// Keyword
//
#define READ_KEYWORD 0x1
#define WRITE_KEYWORD 0x2
#define LOCAL_KEYWORD 0x4
#define REMOTE_KEYWORD 0x8

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR TransferEvent = {0x1, 0x0, 0x0, 0x4, 0x0, 0x0, 0x5};
#define TransferEvent_value 0x1
#define MSG_Provider_Name                    0x90000001L
#define MSG_Event_WhenToTransfer             0xB0000001L
#define MSG_Map_Download                     0xD0000001L
#define MSG_Map_Upload                       0xD0000002L
#define MSG_Map_UploadReply                  0xD0000003L
#define MSG_Map_Sunday                       0xF0000001L
#define MSG_Map_Monday                       0xF0000002L
#define MSG_Map_Tuesday                      0xF0000003L
#define MSG_Map_Wednesday                    0xF0000004L
#define MSG_Map_Thursday                     0xF0000005L
#define MSG_Map_Friday                       0xF0000006L
#define MSG_Map_Saturday                     0xF0000007L
```



 

 
