---
description: Открывает экземпляр поставщика билетов на печать.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Функция Биндптпровидерсунк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264343"
---
# <a name="bindptproviderthunk-function"></a>Функция Биндптпровидерсунк

\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows. [**Птопенпровидерекс**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]

Открывает экземпляр поставщика билетов на печать.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзпринтернаме* \[ окне\]
</dt> <dd>

Полное имя очереди печати.

</dd> <dt>

*maxVersion* \[ окне\]
</dt> <dd>

Последняя версия [схемы печати](./printschema.md) , которую поддерживает вызывающий объект.

</dd> <dt>

*префверсион* \[ окне\]
</dt> <dd>

Версия [схемы печати](./printschema.md) , запрошенная вызывающим объектом.

</dd> <dt>

*фпровидер* \[ заполняет\]
</dt> <dd>

Указатель на маркер поставщика билетов на печать.

</dd> <dt>

*уседверсион* \[ заполняет\]
</dt> <dd>

Версия [схемы печати](./printschema.md) , которую будет использовать поставщик билетов на печать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** . Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).

## <a name="remarks"></a>Комментарии

Перед вызовом этой функции вызывающий поток должен инициализировать COM, вызвав [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Схема печати](./printschema.md)
</dt> <dt>

[**птопенпровидерекс**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> </dl>

 

