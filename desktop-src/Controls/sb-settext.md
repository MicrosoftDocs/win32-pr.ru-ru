---
title: Сообщение SB_SETTEXT (Коммктрл. h)
description: Задает текст в указанной части окна состояния.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Элементы управления Windows для SB_SETTEXT сообщений
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136823"
---
# <a name="sb_settext-message"></a>\_Сообщение SB SETTEXT

Задает текст в указанной части окна состояния.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Лобите**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) слово низкого порядка Указывает отсчитываемый от нуля индекс части, которую нужно задать. Если **лобите** имеет значение SB \_ симплеид, то окно состояния считается строкой состояния простого режима, то есть строкой состояния только с одной частью.

[**Хибите**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) слово низкого порядка указывает тип операции рисования. Этот параметр может принимать одно из указанных ниже значений.

Слово « *wParam* » высокого порядка не учитывается.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <dt><strong>0,0</strong></dt> </dl></td>
<td>Текст отображается с границей, которая отображается ниже плоскости окна.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <dt><strong>SBT_NOBORDERS</strong></dt> </dl></td>
<td>Текст отображается без границ.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <dt><strong>SBT_OWNERDRAW</strong></dt> </dl></td>
<td>Текст рисуется родительским окном. <br/>
<blockquote>
[!Note]<br />
Строка состояния простого режима не поддерживает рисование владельцем.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>Текст отображается с границей, которая отображается выше плоскости окна.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <dt><strong>SBT_RTLREADING</strong></dt> </dl></td>
<td>Текст будет отображаться в обратном направлении к тексту в родительском окне.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <dt><strong>SBT_NOTABPARSING</strong></dt> </dl></td>
<td>Символы табуляции игнорируются.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает текст для установки. Если аргумент *wParam* имеет значение SBT \_ овнердрав, этот параметр представляет 32 бит данных. Родительское окно должно интерпретировать данные и нарисовать текст при получении сообщения [**WM \_ DRAWITEM**](wm-drawitem.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Сообщение сделает недействительным измененную часть окна, что привело бы к отображению нового текста, когда окно затем получит сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) .

Нормальный отображаемый текст Windows слева направо (LTR). Windows может быть *зеркальным* отображением таких языков, как иврит или арабский, которые читаются справа налево. Если задан параметр SBT \_ RTLREADING, строка *lParam* будет считаться в обратном направлении от текста в родительском окне.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **SB \_ СЕТТЕКСТВ** (Юникод) и **SB \_ сеттекста** (ANSI)<br/>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SB ( \_ SMS)**](sb-gettext.md)
</dt> </dl>

 

