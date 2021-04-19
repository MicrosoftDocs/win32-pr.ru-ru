---
description: Интерфейсы API защиты от потери данных (DLP) Endpoint позволяют приложениям уведомлять ОС до и после определенных операций, таких как открытие или сохранение файла.
title: Защита от потери данных конечной точки
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 3b8576f9eadd0037eca56c0ba183ea1d1825679a
ms.sourcegitcommit: 8b543a86e551cb5b4270a3cc3590ad0758fb6156
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "107526083"
---
# <a name="endpoint-data-loss-prevention"></a>Защита от потери данных конечной точки

Windows 10 реализует механизмы, помогающие предотвратить потери данных для конфиденциальных файлов. Интерфейсы API защиты от потери данных (DLP) Endpoint позволяют приложениям уведомлять ОС до и после определенных операций, таких как открытие или сохранение файла. Эти уведомления служат в качестве подсказок, которые позволяют системе оптимизировать операции потери данных.

## <a name="location-of-the-dlp-dll"></a>Расположение библиотеки DLL DLP

Так как библиотека DLL защиты конечной точки не входит в состав Windows SDK, приложениям потребуется вручную загрузить библиотеку DLL во время выполнения. Путь к расположению библиотеки DLL хранится в реестре. В следующей таблице перечислены разделы и значения реестра, в которых хранятся эти сведения. Эти пути определяются как константы в приведенном ниже листинге кода ендпоинтдлп. h для удобства разработчиков.

| Константа | Значение | Описание   |
|----------|-------|---------------|
| ENDPOINTDLP_DLL_NAME | "EndpointDlp.dll" | Имя DLL-библиотеки DLP конечной точки, предоставляющей API |
| ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY | "Программное обеспечение \\ \\ защитника Microsoft Windows" | Раздел реестра защитника Windows в HKLM, где хранятся параметры DLP конечной точки |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY | Значение ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |  Путь реестра в разделе HKLM Key, из которого можно получить расположение установки EndpointDlp.dll |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE | InstallLocation | Значение реестра в разделе ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY, в котором хранится расположение установки EndpointDlp.dll |
| ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX | с | На платформах x64 объедините этот каталог, чтобы получить версию x86 EndpointDlp.dll |

## <a name="check-if-endpoint-dlp-is-enabled"></a>Проверка включения DLP в конечной точке

Чтобы определить, включена ли в системе поддержка конечной точки DLP, проверьте следующее значение раздела реестра. 

| Константа | Значение | Описание   |
|----------|-------|---------------|
| ENDPOINTDLP_ENABLED_FLAG_REGKEY |  " \\ Функции" | Путь к ключу флага включения защиты от потери данных в разделе (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |
| ENDPOINTDLP_ENABLED_FLAG_REGVALUE | "Сенседлпенаблед" | Значение реестра в разделе ENDPOINTDLP_ENABLED_FLAG_REGKEY, содержащее раздел реестра с флагом DLP Enabled

## <a name="endpoint-dlp-apis"></a>API-интерфейсы защиты конечной точки

В следующих таблицах перечислены интерфейсы API, предоставляемые библиотекой DLL DLP конечной точки.

### <a name="initialization-and-versioning"></a>Инициализация и управление версиями

| API | Описание |
|-----|-------------|
| [длпинитиализинфорцементмоде](endpointdlp-dlpinitializeenforcementmode.md)                       | Уведомляет систему о требуемых режимах применения для набора операций защиты от потери данных в конечной точке.                                  |
| [длпжетенфорцементапиверсион](endpointdlp-dlpgetenforcementapiversion.md)                       | Извлекает версию API защиты от потери данных для конечной точки на текущем устройстве.                                  |


### <a name="document-operations"></a>Операции с документом

| API | Описание |
|-----|-------------|
| [длпнотифипреопендокумент](endpointdlp-dlpnotifypreopendocument.md) | Предоставляет системе сведения о документе до запуска операции открытия. |
| [длпнотифипостопендокумент](endpointdlp-dlpnotifypostopendocument.md) | Предоставляет системе сведения о документе после завершения операции открытия.  |
| [длпнотификлоседокумент](endpointdlp-dlpnotifyclosedocument.md)                       | Предоставляет системе сведения о документе до инициирования операции закрытия документа.                                  |
| [длпнотифипреопендокументфиле](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Предоставляет системе сведения о документе до запуска операции открытия.  |
| [длпнотифипостопендокументфиле](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Предоставляет системе сведения о документе после завершения операции открытия.                                  |
| [длпнотификлоседокументфиле](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Предоставляет системе сведения о документе до инициирования операции закрытия документа.                                  |

### <a name="save-as-operations"></a>Сохранить как операции
| API | Описание |
|-----|-------------|
| [длпнотифипресавеасдокумент](endpointdlp-dlpnotifypresaveasdocument.md)                       | Предоставляет системе сведения о документе до инициации операции сохранения.                                  |
| [длпнотифипостсавеасдокумент](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Предоставляет системе сведения о документе после завершения операции Сохранить как.                                  |


### <a name="drag-and-drop-operations"></a>Операции перетаскивания

| API | Описание |
|-----|-------------|
| [длпнотифентердроптаржет](endpointdlp-dlpnotifyenterdroptarget.md)                       | Предоставляет системе сведения о документе при входе в цель перетаскивания.                                  |
| [длпнотифилеаведроптаржет](endpointdlp-dlpnotifyleavedroptarget.md)                       | Предоставляет системе сведения о документе при выходе из целевого объекта перетаскивания.                                  |
| [длпнотифипредрагдроп](endpointdlp-dlpnotifypredragdrop.md)                         | Предоставляет системе сведения о документе до инициирования операции перетаскивания.  |
| [длпнотифипостдрагдроп](endpointdlp-dlpnotifypostdragdrop.md)                         | Предоставляет системе сведения о документе после завершения операции перетаскивания.  |


### <a name="clipboard-operations"></a>Clipboard - операции

| API | Описание |
|-----|-------------|
| [длпнотифипрекопитоклипбоард](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Предоставляет системе сведения о документе до инициирования операции копирования в буфер обмена.  |
| [длпнотифипосткопитоклипбоард](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Предоставляет системе сведения о документе после завершения операции копирования в буфер обмена.  |
| [длпнотифипрепастефромклипбоард](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Предоставляет системе сведения о документе до начала операции вставки из буфера обмена.  |
| [длпнотифипостпастефромклипбоард](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Предоставляет системе сведения о документе после завершения операции вставки из буфера обмена.                                  |
| [длпнотифипостсташклипбоард](endpointdlp-dlpnotifypoststashclipboard.md)                       | Предоставляет систему со сведениями о состоянии после завершения операции скрытого буфера обмена.                                  |
| [длпнотифипресташклипбоард](endpointdlp-dlpnotifyprestashclipboard.md)                       | Уведомляет систему перед инициированием операции скрытого буфера обмена.                                  |
| [длпмустпастефромсистемклипбоард](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Определяет, следует ли приложению извлекать данные из системного буфера обмена, вместо того чтобы брать их из внутреннего кэша.                                  |

### <a name="print-operations"></a>Операции печати

| API | Описание |
|-----|-------------|
| [длпнотифипрепринт](endpointdlp-dlpnotifypreprint.md)                         | Предоставляет системе сведения о документе до начала операции печати.  |
| [длпнотифипостстартпринт](endpointdlp-dlpnotifypoststartprint.md)                       | Предоставляет системе сведения о документе после запуска операции печати.                                  |
| [длпнотифипостпринт](endpointdlp-dlpnotifypostprint.md)                       | Предоставляет системе сведения о документе после завершения операции печати.                                  |

## <a name="endpoint-dlp-example-header"></a>Заголовок Endpoint DLP, пример

Поскольку заголовок DLP конечной точки не включен в Windows SDK, необходимо создать файл заголовка самостоятельно, чтобы получить сигнатуры API для использования в реализации. Для удобства мы предоставляем пример кода, который можно скопировать и вставить в приложение. Помимо объявлений функций, этот листинг кода также определяет полезные константы, такие как сведения об управлении версиями и пути к разделам реестра.

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


/*
Function description:
    Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.

Parameters:
    None

Return:
    TRUE if calling into the OS clipboard is mandatory, FALSE otherwise
*/
BOOL WINAPI DlpMustPasteFromSystemClipboard();

```


