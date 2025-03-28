<asp:TemplateField HeaderText="Attachment" SortExpression="Present" HeaderStyle-Width="15%" ItemStyle-HorizontalAlign="Center">
    <ItemTemplate>
        <span class="text-danger">
            <asp:LinkButton ID="LblBonus_Attachment" runat="server" CausesValidation="False" 
                CommandArgument='<%# Eval("Bonus_Attachment") %>' OnClick="LblBonus_Attachment_Click"
                CommandName="Download" 
                Text='<%# Eval("Bonus_Attachment").ToString().Length >= 25 ? Eval("Bonus_Attachment").ToString().Substring(37) : Eval("Bonus_Attachment").ToString() %>' />
        </span>
        <asp:FileUpload runat="server" ID="Bonus_Attachment" CssClass="form-control form-control-sm" 
            Font-Size="X-Small" AllowMultiple="true" Height="5%" />
        
        <%-- Validation removed --%>
        <%-- <asp:CustomValidator ID="CustomValidatorBonusAttach" runat="server" ErrorMessage="*" 
            ClientValidationFunction="Validate" ControlToValidate="Bonus_Attachment" 
            ValidationGroup="BtnSubmit" Display="Dynamic" ValidateEmptyText="true" 
            ForeColor="Red" SetFocusOnError="true"></asp:CustomValidator> --%>
    </ItemTemplate>
</asp:TemplateField>
