---
title: Функция Енумлайаутортипфорсетуп
description: Перечисляет установленные раскладки клавиатуры и текстовые службы для пользовательского интерфейса установки или OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Платформа текстовых служб Енумлайаутортипфорсетуп Function
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681856"
---
# <a name="enumlayoutortipforsetup-function"></a>Функция Енумлайаутортипфорсетуп

Перечисляет установленные раскладки клавиатуры и текстовые службы для пользовательского интерфейса установки или OOBE.

## <a name="syntax"></a>Синтаксис


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*LangID* \[ окне\]
</dt> <dd>

Идентификатор языка элемента для перечисления.

</dd> <dt>

*плайаутортип* \[ заполняет\]
</dt> <dd>

Указатель на буфер, который получает массив структур ЛАЙАУТОРТИП. Может иметь **значение NULL** , чтобы получить количество элементов.

</dd> <dt>

*убуфленгс* \[ окне\]
</dt> <dd>

Длина буфера, на который указывает *плайаутортип*. Это пропускается, если *плайаутортип* имеет **значение NULL**.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Не используется. Это значение должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если *плайаутортип* имеет **значение NULL**, число элементов клавиатуры, зарегистрированных в системе; в противном случае число элементов клавиатуры, копируемых в *плайаутортип*.

## <a name="remarks"></a>Комментарии

Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL. Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Определение ЛАЙАУТОРТИП:

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

