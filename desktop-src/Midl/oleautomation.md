---
title: oleautomation - атрибут
description: MIDL oleautomation атрибут и совместимость с автоматизацией.
ms.assetid: 4a1c9a02-d637-4595-87b3-5fe903149357
keywords:
- атрибут oleautomation MIDL
topic_type:
- apiref
api_name:
- oleautomation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827aba4cb0871f7130e658299c6d8836557a156
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069985"
---
# <a name="oleautomation-attribute"></a>oleautomation - атрибут

Атрибут **oleautomation** указывает, что интерфейс совместим с автоматизацией.

``` syntax
[ 
    oleautomation, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
    ...
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Строка UUID* 
</dt> <dd>

Указывает строку UUID, созданную служебной программой uuidgen.

</dd> <dt>

*Interface-список атрибутов* 
</dt> <dd>

Указывает другие атрибуты, применяемые к интерфейсу в целом.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя интерфейса.

</dd> <dt>

*базовый интерфейс* 
</dt> <dd>

Указывает имя интерфейса автоматизации, из которого этот производный интерфейс наследует функции члена, коды состояния и атрибуты интерфейса. Все интерфейсы автоматизации являются производными от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) или [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметры и возвращаемые типы, указанные для членов интерфейса **\[ oleautomation \]** , должны быть совместимы с автоматизацией, как указано в следующей таблице.



| Тип                                            | Описание                                                                                                                                                                                                   |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **boolean**                                     | Элемент данных, который может иметь значение VARIANT \_ true или Variant \_ false. Размер соответствует типу VARIANT \_ bool.                                                                                                     |
| **unsigned char**                               | 8-разрядный элемент данных без знака.                                                                                                                                                                                     |
| **double**                                      | 64-битное число с плавающей запятой IEEE.                                                                                                                                                                            |
| **float**                                       | 32-битное число с плавающей запятой IEEE.                                                                                                                                                                            |
| **int**                                         | Целое число со знаком, размер которого зависит от системы. На 32-разрядных платформах MIDL интерпретирует [**int**](int.md) как 32-разрядное целое число со знаком.                                                                               |
| **long**                                        | 32-разрядное целое число со знаком.                                                                                                                                                                                        |
| **short**                                       | 16-разрядное целое число со знаком.                                                                                                                                                                                        |
| **ОСВОБОЖДАЕМОЙ**                                        | Строка с префиксом длины, как описано в разделе "Автоматизация" раздела [BSTR](/previous-versions/windows/desktop/automat/bstr).                                                                                                    |
| **CURRENCY**                                    | 8-байтовое фиксированное число с плавающей запятой.                                                                                                                                                                          |
| **DATE**                                        | 64-разр. дробное число дней с плавающей запятой с 30 декабря 1899 г.                                                                                                                                     |
| **SCODE**                                       | Для 16-разрядных систем — встроенный тип ошибок, соответствующий \_ ошибке VT.                                                                                                                                         |
| **Перечисление typedef** В  *менум*                      | Целое число со знаком, размер которого зависит от системы.                                                                                                                                                               |
| **Интерфейс IDispatch \***                      | Указатель на интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ Dispatch).                                                                                                                |
| **Интерфейс IUnknown \***                       | Указатель на интерфейс, который не является производным от [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ Unknown). (Любой интерфейс OLE может быть представлен интерфейсом [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .) |
| **диспетчерский интерфейс** В  *TypeName \**                | Указатель на интерфейс, производный от [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (VT \_ Dispatch).                                                                                                    |
| **Coclass** В  *TypeName \**                      | Указатель на имя сокласса (VT \_ Unknown).                                                                                                                                                                      |
| **\[ \] интерфейс oleautomation** в   *TypeName \** | Указатель на интерфейс, производный от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).                                                                                                                                      |
| **SAFEARRAY**(*TypeName*)                       | *TypeName* — любой из приведенных выше типов. Массив этих типов.                                                                                                                                                   |
| **Имени \***                                 | *TypeName* — любой из приведенных выше типов. Указатель на тип.                                                                                                                                                      |
| **Десятичное число**                                     | 96-битовое целое число без знака, масштабируемое по переменной степени 10. Тип данных Decimal, предоставляющий размер и масштаб для числа (как в координатах).                                                       |



 

Параметр совместим с автоматизацией, если он имеет тип, совместимый с автоматизацией, указатель на тип, совместимый с автоматизацией, или SAFEARRAY типа, совместимого с автоматизацией.

Тип возвращаемого значения совместим с автоматизацией, если его тип — HRESULT, SCODE или [**void**](void.md). Однако MIDL требует, чтобы методы интерфейса возвращали HRESULT или SCODE. Возврат значения **void** приводит к ошибке компилятора.

Элемент совместим с автоматизацией, если его возвращаемый тип и все его параметры совместимы с автоматизацией.

Интерфейс, совместимый с автоматизацией, если он является производным от [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) или [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), имеет атрибут **\[ oleautomation \]** , а все его записи VTBL совместимы с автоматизацией. Для 32-разрядных платформ соглашение о вызовах для всех методов в интерфейсе должно быть STDCALL. Для 16-разрядных систем все методы должны иметь соглашение о вызовах CDECL.

Каждый [**disp-интерфейс**](dispinterface.md) является неявно совместимым с автоматизацией. Поэтому не следует использовать атрибут **\[ oleautomation \]** в **интерфейсе DISP**.

Атрибут **\[ oleautomation \]** недоступен при компиляции с помощью параметра [**/ОСФ**](-osf.md) компилятора MIDL.

### <a name="flags"></a>Флаги

ТИПЕФЛАГ \_ фолеаутоматион

## <a name="examples"></a>Примеры

``` syntax
library Hello
{
    importlib("stdole32.tlb");
    [
        uuid(12345678-1234-1234-1234-123456789ABC),
        helpstring("Application object for the Hello application."),
        oleautomation,
        dual
    ]
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }

    // Other library definition statements.
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**/осф**](-osf.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> </dl>

 

 