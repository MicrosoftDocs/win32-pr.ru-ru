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
# <a name="wzcenuminterfaces-function"></a><span data-ttu-id="0f692-103">Функция Взценуминтерфацес</span><span class="sxs-lookup"><span data-stu-id="0f692-103">WZCEnumInterfaces function</span></span>

<span data-ttu-id="0f692-104">\[**Взценуминтерфацес** больше не поддерживается в Windows Vista и windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0f692-104">\[**WZCEnumInterfaces** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0f692-105">Вместо этого используйте функцию [**вланенуминтерфацес**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) .</span><span class="sxs-lookup"><span data-stu-id="0f692-105">Instead, use the [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) function.</span></span> <span data-ttu-id="0f692-106">Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="0f692-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="0f692-107">Функция **взценуминтерфацес** перечисляет все интерфейсы беспроводной локальной сети, управляемые службой настройки беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="0f692-107">The **WZCEnumInterfaces** function enumerates all of the wireless LAN interfaces managed by the Wireless Zero Configuration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f692-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f692-108">Syntax</span></span>


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a><span data-ttu-id="0f692-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f692-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f692-110">*псрваддр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f692-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f692-111">Указатель на строку, содержащую имя компьютера, на котором должна быть выполнена эта функция.</span><span class="sxs-lookup"><span data-stu-id="0f692-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="0f692-112">Если этот параметр имеет **значение NULL**, служба настройки беспроводной связи будет перечисляться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0f692-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is enumerated on the local computer.</span></span>

<span data-ttu-id="0f692-113">Если указанный параметр *псрваддр* является удаленным компьютером, удаленный компьютер должен поддерживать удаленные вызовы RPC.</span><span class="sxs-lookup"><span data-stu-id="0f692-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="0f692-114">*пинтфс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0f692-114">*pIntfs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f692-115">Указатель на структуру [**\_ \_ таблицы ключей интфс**](intfs-key-table.md) , содержащую таблицу ключевых сведений для всех интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0f692-115">A pointer to a [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure that contains a table of key information for all interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f692-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f692-116">Return value</span></span>

<span data-ttu-id="0f692-117">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0f692-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0f692-118">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="0f692-118">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="0f692-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0f692-119">Return code</span></span>                                                                                               | <span data-ttu-id="0f692-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0f692-120">Description</span></span>                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f692-121"><dt>**некоторая ошибка в \_ \_ корзине**</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-121"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="0f692-122">Блоки управления хранилищем были уничтожены.</span><span class="sxs-lookup"><span data-stu-id="0f692-122">The storage control blocks were destroyed.</span></span> <span data-ttu-id="0f692-123">Эта ошибка возвращается, если служба настройки беспроводной связи не инициализирует внутренние объекты.</span><span class="sxs-lookup"><span data-stu-id="0f692-123">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/> |
| <dl> <span data-ttu-id="0f692-124"><dt>**RPC \_ S \_ Unknown, \_ Если**</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-124"><dt>**RPC\_S\_UNKNOWN\_IF**</dt></span></span> </dl>        | <span data-ttu-id="0f692-125">Неизвестный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0f692-125">The interface is unknown.</span></span><br/> <span data-ttu-id="0f692-126">Эта ошибка возвращается, если служба настройки беспроводной связи не запущена.</span><span class="sxs-lookup"><span data-stu-id="0f692-126">This error is returned if the Wireless Zero Configuration service is not started.</span></span><br/>                             |
| <dl> <span data-ttu-id="0f692-127"><dt>**\_ \_ пустой \_ указатель ссылки RPC \_ X**</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-127"><dt>**RPC\_X\_NULL\_REF\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="0f692-128">Заглушке передан пустой указатель ссылки.</span><span class="sxs-lookup"><span data-stu-id="0f692-128">A null reference pointer was passed to the stub.</span></span><br/> <span data-ttu-id="0f692-129">Эта ошибка возвращается, если параметр *пинтфс* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0f692-129">This error is returned if the *pIntfs* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="0f692-130"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-130"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="0f692-131">Недостаточно памяти для обработки этого запроса и выделения памяти для результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="0f692-131">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0f692-132"><dt>**\_Состояние RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-132"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="0f692-133">Различные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="0f692-133">Various error codes.</span></span><br/>                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="0f692-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f692-134">Remarks</span></span>

<span data-ttu-id="0f692-135">Перед вызовом функции **взценуминтерфацес** необходимо задать значение 0 для элемента **двнуминтфс** в структуре [**\_ \_ таблицы ключей интфс**](intfs-key-table.md) , на которую указывает *пинтф* .</span><span class="sxs-lookup"><span data-stu-id="0f692-135">The **dwNumIntfs** member of the [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure pointed to by *pIntf* must be set to 0 before calling the **WZCEnumInterfaces** function.</span></span> <span data-ttu-id="0f692-136">Кроме того, элемент **пинтфс** должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0f692-136">Also, the **pIntfs** member must be set to **NULL**.</span></span>

<span data-ttu-id="0f692-137">При последующих вызовах других функций беспроводной настройки, приложение должно указать интерфейс, на котором он работает, предоставив соответствующие ключевые сведения, возвращаемые функцией **взценуминтерфацес** .</span><span class="sxs-lookup"><span data-stu-id="0f692-137">For subsequent calls to other Wireless Zero Configuration functions, an application must identify the interface it is operating on by providing relevant key information returned by the **WZCEnumInterfaces** function.</span></span>

<span data-ttu-id="0f692-138">Если **взценуминтерфацес** возвращает ошибку \_ успешно, вызывающий объект должен вызвать [**функции LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) , чтобы освободить внутренние буферы, выделенные для данных, возвращаемых после того, как эти сведения больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="0f692-138">If the **WZCEnumInterfaces** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="0f692-139">Файл заголовка *взксапи. h* и файл библиотеки импорта *взксапи. lib* недоступны в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0f692-139">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0f692-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="0f692-140">Examples</span></span>

<span data-ttu-id="0f692-141">В следующем примере перечисляются интерфейсы беспроводной локальной сети на локальном компьютере, управляемом службой настройки беспроводной связи, и выводится значение идентификатора GUID интерфейса для каждого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0f692-141">The following example enumerates the wireless LAN interfaces on the local computer managed by the Wireless Zero Configuration service and prints out the value for interface GUID for each interface.</span></span>

> [!Note]  
> <span data-ttu-id="0f692-142">Этот пример завершится сбоем в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="0f692-142">This example will fail on Windows Vista and later .</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="0f692-143">Требования</span><span class="sxs-lookup"><span data-stu-id="0f692-143">Requirements</span></span>



| <span data-ttu-id="0f692-144">Требование</span><span class="sxs-lookup"><span data-stu-id="0f692-144">Requirement</span></span> | <span data-ttu-id="0f692-145">Значение</span><span class="sxs-lookup"><span data-stu-id="0f692-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f692-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f692-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0f692-147">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f692-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0f692-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f692-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0f692-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f692-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0f692-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0f692-150">End of client support</span></span><br/>    | <span data-ttu-id="0f692-151">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="0f692-151">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="0f692-152">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0f692-152">End of server support</span></span><br/>    | <span data-ttu-id="0f692-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f692-153">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="0f692-154">Header</span><span class="sxs-lookup"><span data-stu-id="0f692-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f692-155"><dt>Взксапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-155"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f692-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f692-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f692-157"><dt>Взксапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-157"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f692-158">DLL</span><span class="sxs-lookup"><span data-stu-id="0f692-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f692-159"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f692-159"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f692-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f692-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f692-161">**\_Таблица ключей \_ интфс**</span><span class="sxs-lookup"><span data-stu-id="0f692-161">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="0f692-162">**\_запись ключа \_ intf**</span><span class="sxs-lookup"><span data-stu-id="0f692-162">**INTF\_KEY\_ENTRY**</span></span>](intf-key-entry.md)
</dt> <dt>

[<span data-ttu-id="0f692-163">**взцеаполжетинтерфацепарамс**</span><span class="sxs-lookup"><span data-stu-id="0f692-163">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="0f692-164">**взккуеринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="0f692-164">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="0f692-165">**взкрефрешинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="0f692-165">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
