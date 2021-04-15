---
description: Создает защищенные выходные объекты для устройства вывода.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Функция Креатеопмпротектедаутпутс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539617"
---
# <a name="createopmprotectedoutputs-function"></a>Функция Креатеопмпротектедаутпутс

> [!IMPORTANT]
> Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера. Приложения не должны вызывать эту функцию.

 

Создает защищенные выходные объекты для устройства вывода.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстрдевиценаме* \[ окне\]
</dt> <dd>

Указатель на [**\_ строковую структуру Юникода**](/windows/win32/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*вос* \[ окне\]
</dt> <dd>

Член перечисления **\_ \_ \_ \_ семантики вывода видео дксгкмдт ОПМ** , указывающий, будет ли защищенный выход иметь семантику (Копп) или семантику ОПМ.

</dd> <dt>

*двопмпротектедаутпутаррайсизе* \[ окне\]
</dt> <dd>

Число элементов в массиве *похопмпротектедаутпутаррай* .

</dd> <dt>

*пдвнумопмпротектедаутпутсинаррай* \[ заполняет\]
</dt> <dd>

Получает число элементов, которые функция копирует в массив *похопмпротектедаутпутаррай* .

</dd> <dt>

*похопмпротектедаутпутаррай* \[ заполняет\]
</dt> <dd>

Массив, который получает дескрипторы для защищенных выходных объектов. Каждый обработчик должен быть освобожден путем вызова [**дестройопмпротектедаутпут**](destroyopmprotectedoutput.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Комментарии

Вместо использования этой функции приложения должны вызывать одну из следующих функций:

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**опмжетвидеуутпутсфромхмонитор**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции ОПМ](opm-functions.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> </dl>

 

 
