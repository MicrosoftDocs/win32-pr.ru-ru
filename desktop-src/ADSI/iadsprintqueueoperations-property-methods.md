---
title: Методы свойств Иадспринткуеуеоператионс (iAds. h)
description: Методы свойств интерфейса Иадспринткуеуеоператионс считывают и записывают свойства, перечисленные в следующем списке. Дополнительные сведения о методах свойств см. в разделе методы свойств интерфейса.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспринткуеуеоператионс ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989091"
---
# <a name="iadsprintqueueoperations-property-methods"></a>Методы свойств Иадспринткуеуеоператионс

Методы свойств интерфейса [**иадспринткуеуеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) считывают и записывают свойства, перечисленные в следующем списке. Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).

## <a name="properties"></a>Свойства

<dl> <dt>

**Состояние**
</dt> <dd> <dl>

Текущее состояние операций очереди печати. Допустимые значения кода состояния перечислены в следующем списке.

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

**Реклама \_ ПРИНТЕР \_ приостановлен** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

**Реклама \_ \_Ожидание \_ удаления принтера** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

**Реклама \_ \_Ошибка принтера** (0x00000003)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

**Реклама \_ \_ \_ Застревание бумаги в принтере** (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

**Реклама \_ \_ \_ Выходной документ принтера** (0x00000005)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

**Реклама \_ \_Ручной \_ веб-канал принтера** (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

**Реклама \_ \_ \_ Проблема с принтером** (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

**Реклама \_ \_Автономный принтер** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

**Реклама \_ \_ \_ Активный ввод-вывод принтера** (0x00000100)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

**Реклама \_ ПРИНТЕР \_ занят** (0x00000200)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

**Реклама \_ \_Печать принтера** (0x00000400)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

**Реклама \_ \_Выходной \_ лоток принтера \_ полон** (0x00000800)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

**Реклама \_ ПРИНТЕР \_ \_ недоступен** (0x00001000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

**Реклама \_ \_Ожидание печати** (0x00002000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

**Реклама \_ \_Обработка принтера** (0x00004000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

**Реклама \_ \_Инициализация принтера** (0x00008000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

**Реклама \_ \_Прогрев принтера \_** (0x00010000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

**Реклама \_ \_ \_ Мало тонера принтера** (0x00020000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

**Реклама \_ ПРИНТЕР \_ без \_ тонера** (0x00040000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

**Реклама \_ \_Страница принтера \_ : разрыв страницы** (0x00080000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

**Реклама \_ \_ \_ Вмешательство пользователя принтера** (0x00100000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

**Реклама \_ \_ \_ \_ Неиспользуемая память принтера** (0x00200000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

**Реклама \_ \_ \_ Открыта дверца принтера** (0x00400000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

**Реклама \_ \_Сервер принтера \_ неизвестен** (0x00800000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

**Реклама \_ \_Режим энергосбережения \_ принтера** (0x01000000)


</dt> <dd></dd> </dl> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Тип данных скрипта: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Примеры

В следующем Visual Basic примере кода проверяется, что принтер застрял.


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



В следующем примере кода C++ проверяется Застревание принтера.


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                              |
| Header<br/>                   | <dl> <dt>IAds. h</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>     |
| IID<br/>                      | IID \_ иадспринткуеуеоператионс определен как 124BE5C0-156E-11CF-A986-00AA006BC149<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иадспринткуеуе**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**иадспринткуеуеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





