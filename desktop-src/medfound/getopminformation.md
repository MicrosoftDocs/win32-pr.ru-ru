---
description: Отправляет запрос состояния ОПМ в защищенный выходной объект.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: Функция Жетопминформатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bd9912289d17085bf94f3ef8316869ffb29d3a5adead4e10fc0e6d24844f4ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777304"
---
# <a name="getopminformation-function"></a>Функция Жетопминформатион

> [!IMPORTANT]
> Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера. Приложения не должны вызывать эту функцию.

 

Отправляет запрос состояния ОПМ в защищенный выходной объект.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI GetOPMInformation(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE       opoOPMProtectedOutput,
  _In_  const DXGKMDT_OPM_GET_INFO_PARAMETERS   *pParameters,
  _Out_       DXGKMDT_OPM_REQUESTED_INFORMATION *pRequestedInformation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*опупмпротектедаутпут* \[ окне\]
</dt> <dd>

Маркер защищенного выходного объекта. Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).

</dd> <dt>

*ппараметерс* \[ окне\]
</dt> <dd>

Указатель на структуру **параметров дксгкмдт \_ ОПМ \_ Get \_ info \_** , содержащую входные данные для запроса состояния.

</dd> <dt>

*прекуестединформатион* \[ заполняет\]
</dt> <dd>

Указатель на **дксгкмдт ОПМ структуру \_ \_ \_ информации** , которая получает результаты запроса состояния.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Remarks

Приложения должны вызывать [**иопмвидеуутпут:: uninformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) вместо вызова этой функции.

Защищенный выходной объект должен быть создан с семантикой ОПМ. См. [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции ОПМ](opm-functions.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> </dl>

 

 
