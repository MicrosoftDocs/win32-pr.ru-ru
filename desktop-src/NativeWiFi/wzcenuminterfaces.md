---
description: Перечисляет все интерфейсы беспроводной локальной сети, управляемые службой настройки беспроводной связи.
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: Функция Взценуминтерфацес (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEnumInterfaces
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: b2a2c886f59843dd1bf1316053c603faf4cc112a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912519"
---
# <a name="wzcenuminterfaces-function"></a>Функция Взценуминтерфацес

\[**Взценуминтерфацес** больше не поддерживается в Windows Vista и windows Server 2008. Вместо этого используйте функцию [**вланенуминтерфацес**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) . Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]

Функция **взценуминтерфацес** перечисляет все интерфейсы беспроводной локальной сети, управляемые службой настройки беспроводной связи.

## <a name="syntax"></a>Синтаксис


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псрваддр* \[ окне\]
</dt> <dd>

Указатель на строку, содержащую имя компьютера, на котором должна быть выполнена эта функция. Если этот параметр имеет **значение NULL**, служба настройки беспроводной связи будет перечисляться на локальном компьютере.

Если указанный параметр *псрваддр* является удаленным компьютером, удаленный компьютер должен поддерживать удаленные вызовы RPC.

</dd> <dt>

*пинтфс* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**\_ \_ таблицы ключей интфс**](intfs-key-table.md) , содержащую таблицу ключевых сведений для всех интерфейсов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение ошибки \_ Success.

Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов возврата.



| Код возврата                                                                                               | Описание                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**некоторая ошибка в \_ \_ корзине**</dt> </dl>      | Блоки управления хранилищем были уничтожены. Эта ошибка возвращается, если служба настройки беспроводной связи не инициализирует внутренние объекты.<br/> |
| <dl> <dt>**RPC \_ S \_ Unknown, \_ Если**</dt> </dl>        | Неизвестный интерфейс.<br/> Эта ошибка возвращается, если служба настройки беспроводной связи не запущена.<br/>                             |
| <dl> <dt>**\_ \_ пустой \_ указатель ссылки RPC \_ X**</dt> </dl> | Заглушке передан пустой указатель ссылки.<br/> Эта ошибка возвращается, если параметр *пинтфс* имеет **значение NULL**.<br/>                          |
| <dl> <dt>**Ошибка \_ не \_ хватает \_ памяти**</dt> </dl> | Недостаточно памяти для обработки этого запроса и выделения памяти для результатов запроса.<br/>                                                  |
| <dl> <dt>**\_Состояние RPC**</dt> </dl>                | Различные коды ошибок.<br/>                                                                                                                               |



 

## <a name="remarks"></a>Комментарии

Перед вызовом функции **взценуминтерфацес** необходимо задать значение 0 для элемента **двнуминтфс** в структуре [**\_ \_ таблицы ключей интфс**](intfs-key-table.md) , на которую указывает *пинтф* . Кроме того, элемент **пинтфс** должен иметь значение **null**.

При последующих вызовах других функций беспроводной настройки, приложение должно указать интерфейс, на котором он работает, предоставив соответствующие ключевые сведения, возвращаемые функцией **взценуминтерфацес** .

Если **взценуминтерфацес** возвращает ошибку \_ успешно, вызывающий объект должен вызвать [**функции LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) , чтобы освободить внутренние буферы, выделенные для данных, возвращаемых после того, как эти сведения больше не нужны.

> [!Note]  
> Файл заголовка *взксапи. h* и файл библиотеки импорта *взксапи. lib* недоступны в Windows SDK.

 

## <a name="examples"></a>Примеры

В следующем примере перечисляются интерфейсы беспроводной локальной сети на локальном компьютере, управляемом службой настройки беспроводной связи, и выводится значение идентификатора GUID интерфейса для каждого интерфейса.

> [!Note]  
> Этот пример завершится сбоем в Windows Vista и более поздних версиях.

 


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Wzcsapi.h and Wsczapi.lib were never shipped
// So we need to LOadlibrary and call the WZCEnumInterfaces function 
// in Wzcsapi.dll in the 

typedef struct
{
    LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;

typedef struct
{
    DWORD dwNumIntfs;
    PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;

DWORD WZCEnumInterfaces(LPWSTR pSrvAddr, PINTFS_KEY_TABLE pIntfs);

//Define the function prototype
typedef DWORD (CALLBACK* WZCEnumInterfacesType)(LPWSTR, PINTFS_KEY_TABLE);

int wmain()
{
    // Declare and initialize variables.

    DWORD dwResult = 0;
//    int iRet = 0;
    
//    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WZCEnumInterfaces  */
    
    PINTFS_KEY_TABLE pIfList; 
    PINTF_KEY_ENTRY pIfInfo;
    
    BOOL freeResult = FALSE;
    BOOL runTimeLinkSuccess = FALSE; 
    HINSTANCE dllHandle = NULL;              
    WZCEnumInterfacesType WZCEnumInterfacesPtr = NULL;

//    wprintf(L"Sample to test WZCEnumInterface\n");
    
    //Load the dll and keep the handle to it
    dllHandle = LoadLibrary( (LPCWSTR) L"wzcsapi.dll");

    // If the handle is valid, try to get the function address. 
    if (dllHandle == NULL) {
        dwResult = GetLastError();
        wprintf(L"LoadLibrary of wzcsapi.dll failed with error: %d\n", dwResult);
        if (dwResult ==  ERROR_MOD_NOT_FOUND)
            wprintf(L"Error: The specified module could not be found\n");
        return 1;
    }
    else  
    { 
        //Get pointer to our function using GetProcAddress:
        WZCEnumInterfacesPtr = (WZCEnumInterfacesType) GetProcAddress(dllHandle,
         "WZCEnumInterfaces");

        if (WZCEnumInterfacesPtr != NULL)
            runTimeLinkSuccess = TRUE;
        else {
            dwResult = GetLastError();   
            wprintf(L"GetProcAddress of WZCEnumInterfaces failed with error: %d\n", dwResult);
            return 1;
        }    
             
        // The function address is valid, allocate some memory for pIflist
        pIfList = (PINTFS_KEY_TABLE) LocalAlloc(LMEM_ZEROINIT,4096);
        if (pIfList == NULL) {    
            wprintf(L"Unable to allocate memory to store INTFS_KEY_TABLE\n");
            freeResult = FreeLibrary(dllHandle);
            return 1;
        }    

        // If the function address is valid, call the function. 
        if (runTimeLinkSuccess)
        {
            dwResult = WZCEnumInterfacesPtr(NULL, pIfList); 
            if (dwResult != ERROR_SUCCESS)  {
                wprintf(L"WZCEnumInterfaces failed with error: %u\n", dwResult);
                // FormatMessage can be used to find out why the function failed
                  //Free the library:
                freeResult = FreeLibrary(dllHandle);
                return 1;
            }
            else {
                wprintf(L"Num Entries: %lu\n", pIfList->dwNumIntfs);

                for (i = 0; i < (int) pIfList->dwNumIntfs; i++) {
                    pIfInfo = &pIfList->pIntfs[i];
                    if (pIfInfo->wszGuid == NULL)
                        wprintf(L"  InterfaceGUID[%d]: NULL\n",i);
                    else
                        wprintf(L"  InterfaceGUID[%d]: %ws\n",i, pIfInfo->wszGuid);
                    
                }    
            }
            wprintf(L"\n");
        }
        
        freeResult = FreeLibrary(dllHandle);
    }

    if (pIfList != NULL) {
        LocalFree(pIfList);
        pIfList = NULL;
    }
    return 0;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 3 (SP3)<br/>                                                         |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Взксапи. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Взксапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Таблица ключей \_ интфс**](intfs-key-table.md)
</dt> <dt>

[**\_запись ключа \_ intf**](intf-key-entry.md)
</dt> <dt>

[**взцеаполжетинтерфацепарамс**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**взккуеринтерфаце**](wzcqueryinterface.md)
</dt> <dt>

[**взкрефрешинтерфаце**](wzcrefreshinterface.md)
</dt> </dl>

 

 
